---
title: Proxy 物件的設計考慮
description: Proxy 和可存取的物件設計取決於伺服器 UI 元素的設計。 無論設計為何，UI 專案都必須在終結之前通知 proxy 物件，讓 proxy 物件適當地處理來自用戶端的呼叫。
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cd96056f89e1efc18da3e299a76e92c85166efd7067e54f972a69eb8786d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830068"
---
# <a name="design-considerations-for-proxy-objects"></a>Proxy 物件的設計考慮

Proxy 和可存取的物件設計取決於伺服器 UI 元素的設計。 無論設計為何，UI 專案都必須在終結之前通知 proxy 物件，讓 proxy 物件適當地處理來自用戶端的呼叫。

下列清單描述兩種設計可能性：

-   將實 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的程式碼放在與執行使用者介面專案的程式碼相同的模組中，如果使用者介面程式碼容易擴充。 在此情況下，proxy 的意義是「輕量」，因為它所做的只是監視可存取物件的存留期、將呼叫轉送到可存取的物件，然後傳回結果。
-   將實 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 的程式碼放在與執行 proxy 物件的程式碼相同的模組中。 在此情況下，可存取的物件會使用內建函式來取得 UI 元素的相關資訊。

## <a name="trackbar-controls"></a>[請] 控制項

當您在執行資料類型控制時，請使用 **\_ 反向** 的 [資料類型] 的 [tb] 來提供更有意義 此樣式會反轉 [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)所使用的小數位數。

針對沒有此樣式的垂直 trackbars， [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 會在 [頁首] 捲軸位於控制項頂端時傳回零 (0) 。當您將 thumb 朝底部滑動時，這些值就會增加。 使用 **tb \_ 反轉** 樣式時， **IAccessible：： get \_ accValue** 會傳回 100 (100) 當頁首位於頂端時; 當您將頁首移往底部時，會降低數位。

若為不含此樣式的水準 trackbars，當捲軸捲動方塊位於控制項的左邊時，會傳回零 (0) ;當您將 [對齊] 捲軸移至右側時，這些值就會增加。 使用 **tb \_ 反轉** 樣式時， [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 會在 [資料列] 捲軸位於左邊時，傳回 100 (100) ; 當您將 [資料列] 捲軸向右移動時，這些值就會降低。

 

 




