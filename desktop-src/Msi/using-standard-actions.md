---
description: 藉由呼叫 MsiDoAction 函數或在順序資料表中包含動作，在 Windows Installer 中執行動作。
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: 使用標準動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975016"
---
# <a name="using-standard-actions"></a>使用標準動作

藉由呼叫 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函數或在順序資料表中包含動作，在 Windows Installer 中執行動作。 因為大部分的動作都會封裝單一用途，所以使用動作最常見的方式就是將一連串的動作排序成一個序列，以完成較大的工作。 安裝程式有三個標準的最上層動作，這些動作會呼叫一組相關聯的順序資料表。 這些相關聯的順序資料表可能包含標準動作、自訂動作和使用者介面元素。 順序資料表中的每個動作都有相關聯的序號，而且也可以有相關聯的條件運算式。 順序資料表中的所有動作都會依序流覽，而且只有在條件運算式評估為 True 時才會執行。

雖然標準動作可以有與其相關聯的任何序號，但是有許多順序限制必須遵循，才能讓動作正常運作。 例如，您必須在[CostInitialize 動作](costinitialize-action.md)之後呼叫[FileCost 動作](filecost-action.md)。 如需標準動作順序限制的詳細資訊，請參閱 [具有排序限制的動作](actions-with-sequencing-restrictions.md)、 [沒有排序限制的動作](actions-without-sequencing-restrictions.md)，或 [標準動作參考](standard-actions-reference.md)。

下列主題提供有關使用標準動作的詳細資訊。

-   [發佈產品、功能和元件](publishing-products-features-and-components.md)
-   [檔案搜尋](file-searching.md)
-   [檔案成本](file-costing.md)
-   [檔案安裝](file-installation.md)
-   [修改登錄](modifying-the-registry.md)
-   [執行動作](running-actions.md)

另請參閱 [標準動作](about-standard-actions.md) 或 [標準動作參考](standard-actions-reference.md)。

 

 



