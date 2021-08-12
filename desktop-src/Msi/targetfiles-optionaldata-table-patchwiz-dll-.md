---
description: TargetFiles \_ OptionalData 資料表包含目標映射中特定檔案的相關資訊。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 UiCreatePatchPackageEx 函數使用。
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: 'TargetFiles_OptionalData 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5664e2e21968cb3fee5ce3d606dd07008f2436c4b649a7bcefeebd77df9cf6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623733"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>TargetFiles \_ OptionalData 資料表 (Patchwiz.dll) 

TargetFiles \_ OptionalData 資料表包含目標映射中特定檔案的相關資訊。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。

TargetFiles \_ OptionalData 資料表有下列資料行。



| Column        | 類型 | 答案 | Nullable |
|---------------|------|-----|----------|
| 目標        | text | Y   | N        |
| FTK           | text | Y   | N        |
| SymbolPaths   | text |     | Y        |
| IgnoreOffsets | text |     | Y        |
| IgnoreLengths | text |     | Y        |
| RetainOffsets | text |     | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標
</dt> <dd>

TargetImages 資料表的目標資料行的外鍵 [ (Patchwiz.dll) ](targetimages-table-patchwiz-dll-.md)。

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

目標影像的檔案 [資料表](file-table.md) 中的外鍵。

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

此欄位中的值會加入至 [TargetImages 資料表 ](targetimages-table-patchwiz-dll-.md) 之 SymbolPaths 資料行中的分號分隔資料夾清單， (Patchwiz.dll 在產生修補程式時) ，而且可以用來新增特定檔案的符號檔。

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

此欄位中的值是以逗號分隔的範圍位移數位清單，可在目標檔案中忽略範圍。 清單中的範圍順序和數目必須符合 IgnoreLengths 資料行中的專案。 此資料行是選擇性的。

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

此欄位中的值是以逗號分隔的範圍長度清單（以位元組為單位），可忽略目標檔案中的範圍。 清單中的範圍順序和數目必須符合 IgnoreOffsets 資料行中的專案。 此資料行是選擇性的。

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

此欄位中的值是以逗號分隔的範圍位移編號清單，這些範圍是要在目標檔案中保留的範圍。 清單中的範圍順序和數目必須符合[FamilyFileRanges 資料表 (Patchwiz.dll](familyfileranges-table-patchwiz-dll-.md)中對應記錄的 RetainOffsets 資料行中的專案) 

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補選取的檔案區域](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



