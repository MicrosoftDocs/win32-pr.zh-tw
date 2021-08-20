---
description: PATCHWIZ.DLL Windows Installer&160 版發行的版本， \# 3.0 可以自動產生修補程式順序資訊，並將新的修補程式新增至 MsiPatchSequence 資料表。
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: " (PATCHWIZ.DLL) 產生修補程式順序資訊"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03094d9df26f4565db5b3a31c9a27c58a0bb45dac8aac93b2fefce34104d58c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947019"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a> (PATCHWIZ.DLL) 產生修補程式順序資訊

使用 Windows Installer 3.0 發行的[PATCHWIZ.DLL](patchwiz-dll.md)版本可以自動產生修補程式順序資訊，並將新的修補程式新增至[MsiPatchSequence 資料表](msipatchsequence-table.md)。

在 pcp 檔案 \_ 的 [屬性] 資料表中，將 [將資料 \_ 產生 \_ 停用順序] 屬性設定為 1 (一個) ，以防止自動產生修補程式排序資訊。 [](properties-table-patchwiz-dll-.md) 如果這個屬性不存在，則會自動產生和新增資訊。

使用 Windows Installer 3.0 發行的[PATCHWIZ.DLL](patchwiz-dll.md)用來自動產生修補程式排序資訊時，會發生下列情況：

-   針對[TargetImages 資料表](targetimages-table-patchwiz-dll-.md)中所列之目標影像的每個產品代碼，會將新的資料列新增至[MsiPatchSequence 資料表](msipatchsequence-table.md)。
-   在新資料列中加入至 PatchFamily 資料行的值，會對應到 [TargetImages 資料表](targetimages-table-patchwiz-dll-.md)中所列之目標影像的目標產品代碼。
-   在新資料列中加入順序資料行的值，會使用 patch 的目標最高產品版本和產生 patch 的 UTC 時間產生。 序號為 <Product Minor Version> 。 <Build Major Number><時間戳記 1>。 <時間戳記 2>。
    -   第一個欄位是修補程式設為目標之最高版本產品的產品版本。
    -   第二個欄位是修補程式設為目標之最高版本產品的組建主要編號。

    這兩個時間戳記欄位會用於計算國際標準時間 (UTC) 的秒數所需的32位時間戳記。
    > [!Note]  
    > 產品版本的格式如下： <Product Major Version> ... <Product Minor Version> <Build Major Number> <Build Minor Number> ，而且版本號碼為2.1.0.0 的產品版本比產品版本號碼更高1.2.0。0

     

-   MsidbPatchSequenceSupersedeEarlier 屬性會輸入至為 service pack (SP) 或次要升級修補程式所產生的新資料列之 [屬性] 資料行中。 MsidbPatchSequenceSupersedeEarlier 屬性不會加入至 QFE 或小型更新修補程式。
    > [!Note]  
    >  (SP) 的 service pack 應該包含之前發行的所有 Qfe 的修正程式。 但是，如果 patch author 將 [順序 \_ 資料 \_ 取代] 屬性設定為 0 (零) 或 1 (pcp 檔案中的一個) ，則 MsiPatchSequence 資料表中所有資料列的 [屬性] 資料行會設定為 [順序資料取代] 所指定的值 \_ \_ 。 需要更多控制的修補程式作者必須手動撰寫 [屬性] 資料行。

     

如果您在 pcp 檔案中包含 [PatchSequence 資料表](patchsequence-table--patchwiz-dll-.md) ，則 \_ 會忽略 [順序資料 \_ 產生 \_ 已停用] 屬性，並將 PatchSequence 資料表中提供的資訊新增至 patch 的 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。

 

 



