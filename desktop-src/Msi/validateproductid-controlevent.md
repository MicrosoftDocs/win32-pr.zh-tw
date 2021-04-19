---
description: ValidateProductID 事件會將 ProductID 屬性設定為完整的產品識別碼。 如果驗證失敗，則此事件會針對產品識別碼的使用者專案顯示錯誤訊息和強制回應對話方塊。
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971038"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent

ValidateProductID 事件會將 [**ProductID**](productid.md) 屬性設定為完整的產品識別碼。 如果驗證失敗，則此事件會針對產品識別碼的使用者專案顯示錯誤訊息和強制回應對話方塊。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項系結至此事件，用來檢查使用者的產品識別碼專案。 如果使用者的輸入有效，則會開啟下一個對話方塊。

 

 



