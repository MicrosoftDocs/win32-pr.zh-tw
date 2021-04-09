---
description: 次要升級是對許多資源進行變更的更新。
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: 次要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833bb46e2cafe0545f83c0ed0f8ff8aba00f0695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851171"
---
# <a name="minor-upgrades"></a>次要升級

次要升級是對許多資源進行變更的更新。 這些變更都不需要變更 [**ProductCode**](productcode.md)。 更新需要進行 [重大升級](major-upgrades.md) 以變更 **ProductCode**。 次要升級可以用來新增功能和元件，但無法重新組織功能元件樹狀結構。 次要升級可提供產品差異，而不需要實際定義不同的產品。 一般的次要升級包含先前小型更新中的所有修正，並結合成修補程式。 次要升級通常也稱為 service pack (SP) update。 如需哪些更新不需要變更 **ProductCode** 的詳細資訊，請參閱 [變更產品代碼](changing-the-product-code.md)。

次要升級會變更 [**ProductVersion**](productversion.md) 屬性。 變更應用程式的產品版本表示不同的更新具有順序。 例如，如果已有修補程式更新 v 9.0 至9.1 版，而另一個修補程式存在於 patch v 9.1 到 v 9.2，則安裝程式可以在套用修補程式之前先檢查產品版本，以強制執行正確的順序。 這也可防止將 v 9.1 至 v 9.2 修補程式套用至 v 9.0。 針對修補程式，此順序會透過 [修補套件](patch-packages.md)中所含轉換中所設定的產品版本驗證位來強制執行。

次要升級和小型更新的差異在於，次要升級會變更封裝程式碼和產品版本。 請參閱 [小型更新](small-updates.md) ，以取得可由小型更新或次要升級處理之更新類型的指導方針。 次要升級會以完整的產品安裝套件或 [修補套件](patch-packages.md)的形式運送。 不過，次要升級無法針對新版本使用不同的磁片區標籤。

如需有關如何套用次要升級的詳細資訊，請參閱下列主題：

-   [藉由修補產品的本機安裝來套用小型更新](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [重新安裝產品以套用小型更新](applying-small-updates-by-reinstalling-the-product.md)
-   [藉由修補系統管理映射來套用小型更新](applying-small-updates-by-patching-an-administrative-image.md)

 

 



