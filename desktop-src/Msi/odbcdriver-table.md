---
description: ODBCDriver 資料表會列出屬於安裝的 ODBC 驅動程式。
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: ODBCDriver 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eb0da3217d7466fc0beef90933c8a6af32e3d0551ecc6975a31ac55ed2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943119"
---
# <a name="odbcdriver-table"></a>ODBCDriver 資料表

ODBCDriver 資料表會列出屬於安裝的 ODBC 驅動程式。

ODBCDriver 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 驅動程式      | [識別碼](identifier.md) | Y   | N        |
| 元件\_ | [識別碼](identifier.md) | N   | N        |
| Description | [Text](text.md)             | N   | N        |
| 檔案\_      | [識別碼](identifier.md) | N   | N        |
| 檔案 \_ 設定 | [識別碼](identifier.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>司機
</dt> <dd>

驅動程式的內部權杖名稱。 資料表的主鍵

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

元件資料表中的外部索引鍵。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

為此 ODBC 驅動程式註冊的描述。 此值無法當地語系化。

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

驅動程式資料行中所列之驅動程式的 DLL 檔案。 File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。 在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。 \|無法使用 SFN LFN 語法。

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>檔案 \_ 設定
</dt> <dd>

如果驅動程式與驅動程式不同，則為驅動程式的安裝程式 DLL 檔。 File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。 在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。 \|無法使用 SFN LFN 語法。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



