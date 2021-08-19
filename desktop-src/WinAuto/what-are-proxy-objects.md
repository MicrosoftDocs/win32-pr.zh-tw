---
title: 什麼是 Proxy 物件
description: Proxy 物件可做為用戶端與可存取物件之間的媒介。 Proxy 物件的目的是要監視可存取物件的存留期範圍，並只有在未終結時才能將呼叫轉送至可存取的物件。
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf3625bf048241e4ef28163ed3b8ca7916ccc35cccc12e7eac05b2b9b9c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052186"
---
# <a name="what-are-proxy-objects"></a>什麼是 Proxy 物件？

*Proxy* 物件可做為用戶端與可存取物件之間的媒介。 Proxy 物件的目的是要監視可存取物件的存留期範圍，並只有在未終結時才能將呼叫轉送至可存取的物件。

當用戶端呼叫 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性來取得物件的相關資訊時，proxy 物件必須檢查可存取的物件是否仍可供使用。 如果是，proxy 物件會將用戶端的要求傳遞至可存取的物件。 如果可存取物件已損毀 (例如，當有自訂控制項的對話方塊關閉時) ，proxy 物件會傳回錯誤。 為了指出物件已損毀，建議伺服器傳回錯誤碼 **共同的 \_ \_ OBJNOTCONNECTED** ，因為在伺服器呼叫 [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject)之後，元件物件模型 (COM) 會傳回這個錯誤。

Proxy 物件對用戶端而言是透明的。 當用戶端呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)或 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)時，會收到 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的指標。 但是，當用戶端使用這個指標來呼叫任何 **IAccessible** 屬性或方法時，所執行的程式碼就會在 proxy 物件內。

 

 