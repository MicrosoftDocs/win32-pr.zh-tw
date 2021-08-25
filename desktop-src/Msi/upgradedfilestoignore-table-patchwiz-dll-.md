---
description: UpgradedFilesToIgnore 資料表會防止更新相對於目標映射之已升級映射中的特定檔案。
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: 'UpgradedFilesToIgnore 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51143fcf7db350d5ee8aa1e43d49984914bcf9f05a2f8f5f787834a69b7e1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809548"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>UpgradedFilesToIgnore 資料表 (Patchwiz.dll) 

UpgradedFilesToIgnore 資料表會防止更新相對於目標映射之已升級映射中的特定檔案。 在某些情況下，這可能會很有用。 例如，僅供非系統管理安裝使用的修補套件，不需要包含只屬於系統管理映射一部分的修補檔案。 排除只用于系統管理映射的這類檔案，可以減少修補套件的大小;不過，系統管理員應該要知道如何分別更新這些檔案。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。

UpgradedFilesToIgnore 資料表具有下列資料行。



| Column   | 類型 | 答案 | Nullable |
|----------|------|-----|----------|
| 已升級 | text | Y   | N        |
| FTK      | text | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級
</dt> <dd>

UpgradedImages 資料表的升級資料行的外鍵 [ (Patchwiz.dll) ](upgradedimages-table-patchwiz-dll-.md)。 當您將目標升級為升級欄位中指定的映射時，patch 建立工具不會更新 UpgradedFilesToIgnore 資料表之 FTK 資料行中所指定的檔案。 \*在 [已升級] 欄位中輸入 "" 的值，以排除更新所有已升級映射的檔案。

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

已升級之影像的檔案 [資料表](file-table.md) 中的外鍵。 格式為 "" 的值 <prefix> \* 會符合檔案資料表中以該前置詞開頭的所有檔案資料表索引鍵。 星號後面不能有任何文字。

</dd> </dl>

 

 



