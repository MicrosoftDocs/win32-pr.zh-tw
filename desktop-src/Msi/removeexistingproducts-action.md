---
description: RemoveExistingProducts 動作會經歷升級資料表的 ActionProperty 資料行中所列的產品代碼，並叫用並行安裝以依序移除產品。
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: RemoveExistingProducts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3118ebd01aa39b0d9a5dad29ad1c3563c869ed5e0ebc8dfefd5ecd5c89301f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810928"
---
# <a name="removeexistingproducts-action"></a>RemoveExistingProducts 動作

RemoveExistingProducts 動作會經歷 [升級資料表](upgrade-table.md) 的 ActionProperty 資料行中所列的產品代碼，並叫用並行安裝以依序移除產品。 針對每個並行安裝，安裝程式會將 [ [**ProductCode**](productcode.md) ] 屬性設定為 [產品代碼]，並將 [ [**移除**](remove.md) ] 屬性設定為升級資料表之 [移除] 欄位中的值。 如果 [移除] 欄位是空白的，其值會預設為 [全部]，而安裝程式會移除整個產品。

安裝程式只會在第一次安裝產品時執行 RemoveExistingProducts 動作。 它不會在 [維護安裝](maintenance-installation.md) 或卸載期間執行此動作。

## <a name="sequence-restrictions"></a>順序限制

您必須在下列其中一個位置的動作順序中排程 RemoveExistingProducts 動作。

-   在 [InstallValidate 動作](installvalidate-action.md) 與 [InstallInitialize 動作](installinitialize-action.md)之間。 在此情況下，安裝程式會先完全移除舊的應用程式，再安裝新的應用程式。 因為所有重複使用的檔案都必須重新複製，所以此動作的放置效率不佳。
-   在 [InstallInitialize 動作](installinitialize-action.md) 之後，以及產生執行腳本的任何動作之前。
-   介於 [InstallExecute 動作](installexecute-action.md)或 [InstallExecuteAgain 動作](installexecuteagain-action.md)之間，以及 [InstallFinalize 動作](installfinalize-action.md)之間。 通常，最後三個動作會在另一個之後排程： InstallExecute、RemoveExistingProducts 和 InstallFinalize。 在此情況下，會先安裝更新的檔案，然後移除舊的檔案。 但是，如果移除舊的應用程式失敗，則安裝程式會復原舊應用程式的移除以及新應用程式的安裝。
-   在 [InstallFinalize 動作](installfinalize-action.md)之後。 這是最有效率的動作放置位置。 在此情況下，安裝程式會先更新檔案，然後再移除舊的應用程式。 在安裝期間，只會安裝所要更新的檔案。 如果移除舊的應用程式失敗，則安裝程式只會復原舊應用程式的卸載。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 已移除產品。           |



 

## <a name="remarks"></a>備註

Windows安裝程式在執行此動作時，會設定 [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)屬性。

 

 



