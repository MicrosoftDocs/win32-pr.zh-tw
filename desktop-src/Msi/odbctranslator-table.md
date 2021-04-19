---
description: ODBCTranslator 資料表會列出屬於安裝的 ODBC 轉譯。
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: ODBCTranslator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001447"
---
# <a name="odbctranslator-table"></a>ODBCTranslator 資料表

ODBCTranslator 資料表會列出屬於安裝的 ODBC 轉譯。

ODBCTranslator 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| Translator  | [識別碼](identifier.md) | Y   | N        |
| 元件\_ | [識別碼](identifier.md) | N   | N        |
| Description | [Text](text.md)             | N   | N        |
| 檔案\_      | [識別碼](identifier.md) | N   | N        |
| 檔案 \_ 設定 | [識別碼](identifier.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>線上翻譯
</dt> <dd>

Translator 的內部權杖名稱。 資料表的主鍵。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

元件資料表中的外部索引鍵。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

針對此 ODBC 驅動程式轉譯器註冊的描述。 此值無法當地語系化。

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

轉譯器資料行中所列的傳送之 DLL 檔。 File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。 在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。 \|無法使用 SFN LFN 語法。

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>檔案 \_ 設定
</dt> <dd>

Translator 的安裝程式 DLL 檔（如果它與 Translator 資料行不同）。 File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。 在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。 \|無法使用 SFN LFN 語法。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



