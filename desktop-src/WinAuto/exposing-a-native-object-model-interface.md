---
title: 公開原生物件模型介面
description: 如果 UI 元素支援 Microsoft Active Accessibility 或消費者介面自動化以外的原生物件模型，它可以回應 \_ 包含 OBJID NATIVEOM 物件識別碼的 WM GETOBJECT 訊息，藉以公開自訂介面 \_ 。
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021678"
---
# <a name="exposing-a-native-object-model-interface"></a><span data-ttu-id="6e09c-103">公開原生物件模型介面</span><span class="sxs-lookup"><span data-stu-id="6e09c-103">Exposing a Native Object Model Interface</span></span>

<span data-ttu-id="6e09c-104">如果 UI 元素支援 Microsoft Active Accessibility 或消費者介面自動化以外的原生物件模型，它可以回應包含 [**OBJID \_ NATIVEOM**](object-identifiers.md)物件識別碼的 [**WM \_ GETOBJECT**](wm-getobject.md)訊息，藉以公開自訂介面。</span><span class="sxs-lookup"><span data-stu-id="6e09c-104">If a UI element supports a native object model other than Microsoft Active Accessibility or UI Automation, it can expose the custom interface by responding to [**WM\_GETOBJECT**](wm-getobject.md) messages that include the [**OBJID\_NATIVEOM**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="6e09c-105">若要回應，UI 元素應傳回 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函式的呼叫所抓取的值。</span><span class="sxs-lookup"><span data-stu-id="6e09c-105">To respond, the UI element should return the value retrieved by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

<span data-ttu-id="6e09c-106">用戶端可以藉由呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 函式，並將 [**OBJID \_ NATIVEOM**](object-identifiers.md) 指定為第二個參數，從支援原生物件模型的 UI 元素取出介面。</span><span class="sxs-lookup"><span data-stu-id="6e09c-106">A client can retrieve an interface from a UI element that supports a native object model by calling the [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function and specifying [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

 

 




