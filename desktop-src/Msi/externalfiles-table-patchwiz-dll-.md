---
description: ExternalFiles 資料表包含不屬於一般目標映射的特定檔案的相關資訊。
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: 'ExternalFiles 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512792"
---
# <a name="externalfiles-table-patchwizdll"></a>ExternalFiles 資料表 (Patchwiz.dll) 

ExternalFiles 資料表包含不屬於一般目標映射的特定檔案的相關資訊。 這些檔案可能存在於其他產品、升級或修補程式已更新的產品中。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。

ExternalFiles 資料表具有下列資料行。



| Column        | 類型    | 答案 | Nullable |
|---------------|---------|-----|----------|
| 系列        | text    | Y   | N        |
| FTK           | text    | Y   | N        |
| FilePath      | text    | Y   | N        |
| SymbolPaths   | text    |     | Y        |
| IgnoreOffsets | text    |     | Y        |
| IgnoreLengths | text    |     | Y        |
| RetainOffsets | text    |     | N        |
| 單         | 整數 |     | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭
</dt> <dd>

ImageFamilies 資料表之 [家族] 資料行的外鍵 [ (Patchwiz.dll) ](imagefamilies-table-patchwiz-dll-.md)。

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

已升級映射之 .msi 檔案的檔案 [資料表](file-table.md) 中的外鍵。

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath
</dt> <dd>

外部檔案的完整路徑，包括檔案名。 FilePath 欄位是用來尋找 FTK 資料行中指定的檔案。

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

搜尋 FTK 資料行中所指定檔案之符號檔的完整路徑。

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

此欄位中的值是以逗號分隔的範圍位移數位清單，可在外部檔案中忽略範圍。 清單中的範圍順序和數目必須符合 IgnoreLengths 資料行中的專案。 此資料行是選擇性的。

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

此欄位中的值是以逗號分隔的範圍長度清單（以位元組為單位），可忽略外部檔案中的範圍。 清單中的範圍順序和數目必須符合 IgnoreOffsets 資料行中的專案。 此資料行是選擇性的。

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

此欄位中的值是以逗號分隔的範圍位移數位清單，這些範圍是要保留在外部檔案中的範圍。 清單中的範圍順序和數目必須符合 FamilyFileRanges 資料表中對應記錄的 RetainOffsets 資料行中的專案 [ (Patchwiz.dll) ](familyfileranges-table-patchwiz-dll-.md)。

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>以
</dt> <dd>

如果為相同的外部檔案指定了兩個以上的版本，資料表可能會包含 FTK 和數列欄位中具有相符值的多個記錄。 在此情況下，Order 欄位可能會指定建立修補程式時要使用的外部檔案順序。 順序是從最舊到最新版本。

</dd> </dl>

## <a name="remarks"></a>備註

此資料表接受環境變數作為從4.0 版 Patchwiz.dll 開始的路徑。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補選取的檔案區域](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



