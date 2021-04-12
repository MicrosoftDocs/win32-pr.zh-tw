---
title: 什麼是 Proxy 物件
description: Proxy 物件可做為用戶端與可存取物件之間的媒介。 Proxy 物件的目的是要監視可存取物件的存留期範圍，並只有在未終結時才能將呼叫轉送至可存取的物件。
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d54fb20d677f1a417d633242ddf40c704087f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316228"
---
# <a name="what-are-proxy-objects"></a><span data-ttu-id="5fa83-104">什麼是 Proxy 物件？</span><span class="sxs-lookup"><span data-stu-id="5fa83-104">What Are Proxy Objects?</span></span>

<span data-ttu-id="5fa83-105">*Proxy* 物件可做為用戶端與可存取物件之間的媒介。</span><span class="sxs-lookup"><span data-stu-id="5fa83-105">A *proxy* object acts as an intermediary between the client and an accessible object.</span></span> <span data-ttu-id="5fa83-106">Proxy 物件的目的是要監視可存取物件的存留期範圍，並只有在未終結時才能將呼叫轉送至可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="5fa83-106">The purpose of the proxy object is to monitor the life span of the accessible object and to forward calls to the accessible object only if it is not destroyed.</span></span>

<span data-ttu-id="5fa83-107">當用戶端呼叫 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性來取得物件的相關資訊時，proxy 物件必須檢查可存取的物件是否仍可供使用。</span><span class="sxs-lookup"><span data-stu-id="5fa83-107">When a client calls an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) property to get information about an object, the proxy object must check whether the accessible object is still available.</span></span> <span data-ttu-id="5fa83-108">如果是，proxy 物件會將用戶端的要求傳遞至可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="5fa83-108">If it is, the proxy object passes the client's request to the accessible object.</span></span> <span data-ttu-id="5fa83-109">如果可存取物件已損毀 (例如，當有自訂控制項的對話方塊關閉時) ，proxy 物件會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fa83-109">If the accessible object is destroyed (for example, when a dialog box with custom controls is closed), the proxy object returns an error.</span></span> <span data-ttu-id="5fa83-110">為了指出物件已損毀，建議伺服器傳回錯誤碼 **共同的 \_ \_ OBJNOTCONNECTED** ，因為在伺服器呼叫 [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject)之後，元件物件模型 (COM) 會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fa83-110">To indicate that the object has been destroyed, it is recommended that servers return the error code **CO\_E\_OBJNOTCONNECTED** because this error is returned by Component Object Model (COM) after a server calls [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject).</span></span>

<span data-ttu-id="5fa83-111">Proxy 物件對用戶端而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="5fa83-111">The proxy object is transparent to the client.</span></span> <span data-ttu-id="5fa83-112">當用戶端呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)或 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)時，會收到 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5fa83-112">When the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), it receives back a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="5fa83-113">但是，當用戶端使用這個指標來呼叫任何 **IAccessible** 屬性或方法時，所執行的程式碼就會在 proxy 物件內。</span><span class="sxs-lookup"><span data-stu-id="5fa83-113">However, when the client uses this pointer to call any of the **IAccessible** properties or methods, the code that is executed is within the proxy object.</span></span>

 

 