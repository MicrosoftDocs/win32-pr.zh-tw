---
description: ODBCDataSource 資料表會列出屬於安裝的資料來源。
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: ODBCDataSource 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973498"
---
# <a name="odbcdatasource-table"></a>ODBCDataSource 資料表

ODBCDataSource 資料表會列出屬於安裝的資料來源。

ODBCDataSource 資料表具有下列資料行。



| Column            | 類型                         | 答案 | Nullable |
|-------------------|------------------------------|-----|----------|
| DataSource        | [識別碼](identifier.md) | Y   | N        |
| 元件\_       | [識別碼](identifier.md) | N   | N        |
| Description       | [Text](text.md)             | N   | N        |
| DriverDescription | [Text](text.md)             | N   | N        |
| 註冊      | [整數](integer.md)       | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>資料來源
</dt> <dd>

資料來源的內部 token 名稱。 資料表的主鍵。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)中的外部索引鍵。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

為此資料來源註冊的描述。 此值無法當地語系化。 ODBC 資料來源描述不能超過 \_ SQL \_ \_ 的 DSN 長度上限。

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription
</dt> <dd>

可能已預先存在的相關聯驅動程式。 此值無法當地語系化。

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>註冊
</dt> <dd>

此欄位會指定資料來源的註冊類型。



| 常數                                      | 十六進位 | Decimal | Description                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **msidbODBCDataSourceRegistrationPerMachine** | 0x000       | 0       | 每一部電腦都會註冊資料來源。 |
| **msidbODBCDataSourceRegistrationPerUser**    | 0x001       | 1       | 每位使用者都會註冊資料來源。    |



 

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



