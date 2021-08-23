---
description: Patch 資料表指定要接收特定修補程式的檔案，以及媒體映射上修補檔案的實體位置。
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: 修補資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e5f41f206557589bf0b90d9ffb125a80d05d39ce809dc01a8e687a21045475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558458"
---
# <a name="patch-table"></a>修補資料表

Patch 資料表指定要接收特定修補程式的檔案，以及媒體映射上修補檔案的實體位置。

Patch 資料表有下列資料行。



| Column      | 類型                               | 答案 | Nullable |
|-------------|------------------------------------|-----|----------|
| 檔案\_      | [識別碼](identifier.md)       | Y   | N        |
| 順序    | [整數](integer.md)             | Y   | N        |
| PatchSize   | [DoubleInteger](doubleinteger.md) | N   | N        |
| 屬性  | [整數](integer.md)             | N   | N        |
| 標頭      | [二進位](binary.md)               | N   | Y        |
| StreamRef\_ | [識別碼](identifier.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

此修補程式會套用至此資料行中的識別碼所指定的檔案。 這是資料表的主鍵，而且它是 [File 資料表](file-table.md)的外鍵。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

這是修補檔案的位置，以媒體映射上檔案的順序排列。 順序必須對應至修補封裝封包檔中的檔案順序。 這是此資料表的主要索引鍵。 最大限制為32767個檔案，若要建立具有更多檔案的 Windows Installer 封裝，請參閱[撰寫大型封裝](authoring-a-large-package.md)。

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize
</dt> <dd>

此資料行提供以長整數寫入的修補程式大小。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

包含代表 patch 屬性之位旗標的整數。 在此資料行中插入1的值，表示套用此修補程式的失敗不是嚴重錯誤。



| 常數                         | 十六進位 | Decimal | 描述                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (無)                           | 0x000       | 0       | 無法套用此修補程式是嚴重錯誤。                        |
| **msidbPatchAttributesNonVital** | 0x001       | 1       | 指出套用此修補程式的失敗不是嚴重錯誤。 |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>頭
</dt> <dd>

此資料行是用於修補驗證的二進位資料流程修補程式標頭。 如果 StreamRef 資料 \_ 行不是 null，這個資料行應該是 null。 在此情況下，patch 標頭資料流程會儲存在 [MsiPatchHeaders 資料表](msipatchheaders-table.md) 中，以克服 [OLE 限制對資料流程](ole-limitations-on-streams.md)所述的資料流程名稱限制。

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_
</dt> <dd>

MsiPatchHeaders 資料表中的外部索引鍵，指定包含 patch 標頭資料流程的資料列。

</dd> </dl>

## <a name="remarks"></a>備註

此資料表是由 [PatchFiles 動作](patchfiles-action.md)處理。 它通常會透過修補套件的轉換新增至安裝套件。 它通常不會直接撰寫到安裝套件中。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



