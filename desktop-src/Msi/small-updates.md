---
description: 小型更新會變更一或多個太小的應用程式檔，以保證變更產品代碼。
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: 小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 392e19507ca37cf865fab44485b93346dd1ad6cf6d81ada212acb2ec11ddb1c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628168"
---
# <a name="small-updates"></a>小型更新

小型更新會變更一或多個太小的應用程式檔，以保證變更產品代碼。 小型更新通常也稱為快速修正工程， (QFE) 更新。 小型更新不允許重組功能元件樹狀結構。

一般的小型更新只會變更一或兩個檔案或登錄機碼。 因為小型更新會變更 .msi 檔案中的資訊，所以必須變更安裝套件程式碼。 封裝程式碼會儲存在 [摘要資訊資料流程](summary-information-stream.md)的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性中。

產品代碼永遠不會隨著小型更新而變更，因此小型更新所引進的所有變更都必須與 [變更產品代碼](changing-the-product-code.md)中所述的指導方針一致。 更新需要進行 [重大升級](major-upgrades.md) 以變更 [**ProductCode**](productcode.md)。 如果需要在不變更產品代碼的情況下區分產品，請使用 [次要升級](minor-upgrades.md)。

如需如何將小型更新修補套件套用至 Windows Installer 套件的詳細資訊，請參閱[建立小型更新修補程式](creating-a-small-update-patch.md)、[修補產品的本機安裝](applying-small-updates-by-patching-the-local-installation-of-the-product.md)、透過[重新安裝產品來](applying-small-updates-by-reinstalling-the-product.md)套用小型更新，以及藉[由修補系統管理映射](applying-small-updates-by-patching-an-administrative-image.md)以套用小型更新。

 

 



