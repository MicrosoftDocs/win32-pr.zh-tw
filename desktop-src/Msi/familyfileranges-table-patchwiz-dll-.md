---
description: FamilyFileRanges 資料表包含已升級映射的特定檔案的相關資訊，而這些檔案的範圍絕對不應該覆寫。
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: 'FamilyFileRanges 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114561"
---
# <a name="familyfileranges-table-patchwizdll"></a>FamilyFileRanges 資料表 (Patchwiz.dll) 

FamilyFileRanges 資料表包含已升級映射的特定檔案的相關資訊，而這些檔案的範圍絕對不應該覆寫。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。

FamilyFileRanges 資料表具有下列資料行。



| Column        | 類型 | 答案 | Nullable |
|---------------|------|-----|----------|
| 系列        | text | Y   | N        |
| FTK           | text | Y   | N        |
| RetainOffsets | text |     | N        |
| RetainLengths | text |     | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭
</dt> <dd>

ImageFamilies 資料表之 [家族] 資料行的外鍵 [ (Patchwiz.dll) ](imagefamilies-table-patchwiz-dll-.md)。

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

在映射系列中所有已升級影像的檔案 [資料表](file-table.md) 中的外鍵。

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

無法覆寫之範圍的位移。 此欄位中的值是不會在目標檔案中覆寫之範圍的範圍位移數位清單。 清單中的範圍順序和數目必須符合 RetainLengths 資料行中的專案。

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

無法覆寫的範圍長度（以位元組為單位）。 此欄位中的值是要保留于目標檔案之範圍的範圍長度數位清單。 清單中的範圍順序和數目必須符合 RetainOffsets 資料行中的專案。

這些值可以是十進位或十六進位。 [Patchwiz.dll](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，Patchwiz.dll 會將值轉換為 Ulong。

</dd> </dl>

## <a name="remarks"></a>備註

RetainOffsets 和 RetainLengths 中輸入的位移和長度不得指定重迭的範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補選取的檔案區域](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



