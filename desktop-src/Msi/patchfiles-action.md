---
description: PatchFiles 動作會查詢 Patch 資料表，以判斷要套用的修補程式。 PatchFiles 動作也會執行檔案的位元組並存修補。
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: PatchFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6186f150df1871e424b1dc6e4f466d148a1ce2ed51ffd9cd8170a1221e2f0b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082668"
---
# <a name="patchfiles-action"></a>PatchFiles 動作

PatchFiles 動作會查詢 [Patch 資料表](patch-table.md) ，以判斷要套用的修補程式。 PatchFiles 動作也會執行檔案的位元組並存修補。

## <a name="sequence-restrictions"></a>順序限制

如果未安裝要修補的檔案，則 PatchFiles 動作必須在安裝檔案的 [InstallFiles 動作](installfiles-action.md) 之後。 先前安裝的檔案可能會在動作順序中的任何時間點進行修補。 [DuplicateFiles 動作](duplicatefiles-action.md)必須位於 PatchFiles 動作之後，以防止複製未修補的檔案版本。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                    |
|-------|-----------------------------------------------|
| \[1\] | 已修補之檔案的識別碼。                   |
| \[2\] | 保存修補過之檔案的目錄識別碼。 |
| \[3\] | 修補程式的大小（以位元組為單位）。                       |



 

 

 



