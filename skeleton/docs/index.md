## Component Basic Information

| Field Name       | Value                     |
|:-----------------|:--------------------------|
| **Name**         | ${{ values.name }}        |
| **Description**  | ${{ values.description }} |
| **Domain**       | ${{ values.domain }}      |
| **Parent**       | ${{ values.parentRef }}   |
| **_Identifier_** | ${{ values.identifier }}  |
| **_Owner_**      | ${{ values.owner }}       |
| **Depends On**   | ${{ values.dependsOn }}   |
| **Technology**   | Google BigQuery           |
| **Tags**         | {% if values.tags | length > 0 %}{% for i in values.tags %} ${{ i }}; {% endfor %}{% else %}[]{% endif %}      |

{% if values.schemaColumns | length > 0 %}
## Data contract schema

| Column | Data type | Description |
|:-------|:----------|:------------|
{%- for column in values.schemaColumns %}
| ${{ column.name }} | ${{ column.dataType }} | ${{ column.description if column.description else "-" }} |
{%- endfor %}

For other details about each column, please refer to this component `catalog-info.yaml`
{%- endif %}

## Google BigQuery

| Field name      | Example value                                                                                                      |
|:----------------|:-------------------------------------------------------------------------------------------------------------------|
| **Project ID**  | ${{ values.project }}                                                                                              |
| **Dataset**     | {%- if not values.dataset %} <Autogenerated on descriptor generation>  {% else %} ${{values.dataset}} {%- endif %} |
| **Table name**  | ${{ values.tableName }}                                                                                            |
| **View name**   | ${{ values.viewName }}                                                                                             |

## Deployment details 

Deploy this component to automatically create or replace a Google BigQuery View.
