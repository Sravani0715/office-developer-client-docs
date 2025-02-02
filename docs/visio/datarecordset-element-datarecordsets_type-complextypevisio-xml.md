---
title: "DataRecordSet element (DataRecordSets_Type complexType) (Visio XML)"
 
 
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
 
ms.localizationpriority: medium
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: "Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio."
---

# DataRecordSet element (DataRecordSets_Type complexType) (Visio XML)

Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.
  
## Element information

|||
|:-----|:-----|
|**Element type** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schema file** <br/> |VisioSchema15.xsd  <br/> |
|**Document parts** <br/> |recordsets.xml  <br/> |
   
## Definition

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## Elements and attributes

If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section. 
  
### Parent elements

|**Element**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contains all the **DataRecordset** elements in the document. |
   
### Child elements

|**Element**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contains XML that conforms to the ADO classic XML schema for an ADO recordset and that describes the data in the data recordset. |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface. |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting. |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contains all the **DataColumn** elements in a data recordset. |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifies one or more primary-key columns in the data recordset. |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed. |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Maps a data-recordset row to a shape. |
   
### Attributes

|**Attribute**|**Type**|**Required**|**Description**|**Possible values**|
|:-----|:-----|:-----|:-----|:-----|
|Checksum  <br/> |xsd:unsignedInt  <br/> |optional  <br/> |A checksum value, generated by Visio, and based on data-recordset properties. Set this attirbute to 0; Visio recalculates this value at runtime. |Values of the xsd:unsignedInt type. |
|Command  <br/> |xsd:string  <br/> |optional  <br/> |The command string used to query data from the data source. |Values of the xsd:string type. |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |optional  <br/> |The connection ID for the associated **DataConnection** object. Does not exist for XML data sources. |Values of the xsd:unsignedInt type. |
|ID  <br/> |xsd:unsignedInt  <br/> |required  <br/> |The data recordset ID, unique within the document. |Values of the xsd:unsignedInt type. |
|Name  <br/> |xsd:string  <br/> |optional  <br/> |The display (or "friendly") name of the data recordset. |Values of the xsd:string type. |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |optional  <br/> |The next available Visio row ID. |Values of the xsd:unsignedInt type. |
|Options  <br/> |xsd:unsignedInt  <br/> |optional  <br/> |Options to apply to the data recordset. Possible values can be any combination of one or more of those shown in the following table. |Values of the xsd:unsignedInt type. |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |optional  <br/> |How often (in minutes) Visio refreshes the data recordset automatically. This value must be 1 or larger. |Values of the xsd:unsignedInt type. |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |optional  <br/> |Whether the data-reconciliation user interface should be disabled. True (1) to disable the user interface (UI). False (0) to enable the UI. |Values of the xsd:boolean type. |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |optional  <br/> |Whether to overwrite user changes to shape data items in shapes linked to data when the data recordset is refreshed. |Values of the xsd:boolean type. |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |optional  <br/> |Defines how shape-data links are treated when shapes are copied or cut. 1 to replace existing links in the target shape. 0 to maintain existing links in the target shape. |Values of the xsd:unsignedInt type. |
|RowOrder  <br/> |xsd:boolean  <br/> |optional  <br/> |Whether to use the order of the rows in the data recordset as the primary key. True (1) if row IDs are determined by row order. False (0) if row IDs are determined by values in the primary key column(s) of the data recordset. |Values of the xsd:boolean type. |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |optional  <br/> |The date and time the data recordset was last refreshed. |Values of the xsd:dateTime type. |
   

