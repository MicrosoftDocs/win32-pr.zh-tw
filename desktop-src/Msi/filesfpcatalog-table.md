---
description: FileSFPCatalog 資料表會將指定的檔案與系統檔案保護所使用的類別目錄檔案產生關聯。
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: FileSFPCatalog 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bec6e31cba93730cc65b04ffdfb4a509f0cd817ba709cc029edfb47c4c4e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581588"
---
# <a name="filesfpcatalog-table"></a>FileSFPCatalog 資料表

FileSFPCatalog 資料表會將指定的檔案與系統檔案保護所使用的類別目錄檔案產生關聯。

**Windows Vista、Windows Server 2003 和 Windows XP：** 不支援。

FileSFPCatalog 資料表具有下列資料行。



| Column       | 類型                         | 答案 | Nullable |
|--------------|------------------------------|-----|----------|
| 檔案\_       | [識別碼](identifier.md) | Y   | N        |
| SFPCatalog\_ | [檔案名稱](filename.md)     | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

[File 資料表](file-table.md)的外鍵。

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_
</dt> <dd>

[SFPCatalog 資料表](sfpcatalog-table.md)的外鍵。

</dd> </dl>

## <a name="remarks"></a>備註

[InstallSFPCatalogFile 動作](installsfpcatalogfile-action.md)會查詢[Component 資料表](component-table.md)、 [File Table](file-table.md)、FileSFPCatalog table 和[SFPCatalog 資料表](sfpcatalog-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



