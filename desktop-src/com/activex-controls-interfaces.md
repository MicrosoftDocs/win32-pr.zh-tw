---
title: ActiveX 控制項介面
description: ActiveX 控制項介面
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965166"
---
# <a name="activex-controls-interfaces"></a><span data-ttu-id="f5b35-103">ActiveX 控制項介面</span><span class="sxs-lookup"><span data-stu-id="f5b35-103">ActiveX Controls Interfaces</span></span>

<span data-ttu-id="f5b35-104">除了其他在控制項與其用戶端之間進行通訊的機制之外，ActiveX 控制項技術也會指定用於用戶端控制通訊的 [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) 和 [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) 介面。</span><span class="sxs-lookup"><span data-stu-id="f5b35-104">In addition to other mechanisms for communicating between the control and its client, ActiveX controls technology specifies the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) and [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interfaces for client-control communication.</span></span> <span data-ttu-id="f5b35-105">此外，也有適用于簡單控制項容器的 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 介面。</span><span class="sxs-lookup"><span data-stu-id="f5b35-105">There is also the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface for simple control containers.</span></span>

<span data-ttu-id="f5b35-106">不過，這三個介面是控制項特定的，在控制項的內容之外通常並不實用。</span><span class="sxs-lookup"><span data-stu-id="f5b35-106">These three interfaces are, however, specific to controls and are not generally useful outside the context of controls.</span></span> <span data-ttu-id="f5b35-107">這些介面的定義如下。</span><span class="sxs-lookup"><span data-stu-id="f5b35-107">These interfaces are defined as follows.</span></span>

``` syntax
interface IOleControl : IUnknown 
  { 
    HRESULT GetControlInfo([out] CONTROLINFO *pCI); 
    HRESULT OnMnemonic([in] LPMSG pMsg); 
    HRESULT OnAmbientPropertyChange([in] DISPID dispID); 
    HRESULT FreezeEvents([in] BOOL bFreeze); 
  } 
 
interface IOleControlSite : IUnknown 
  { 
    HRESULT OnControlInfoChanged(void); 
    HRESULT LockInPlaceActive([in] BOOL fLock); 
    HRESULT GetExtendedControl([out] IDispatch **ppDisp); 
    HRESULT TransformCoords([in-out] POINTL *pptlHimetric, [in-out] POINTF *pptfContainer, [in] DWORD dwFlags); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg, [in] DWORD grfModifiers); 
    HRESULT OnFocus([in] BOOL fGotFocus); 
    HRESULT ShowPropertyFrame(void); 
  } 
 
interface ISimpleFrameSite : IUnknown 
  { 
    HRESULT PreMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [out] DWORD *pdwCookie); 
    HRESULT PostMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [in] DWORD dwCookie); 
  } 
 
```

<span data-ttu-id="f5b35-108">某些控制項（例如群組方塊）只是其他控制項的簡單容器。</span><span class="sxs-lookup"><span data-stu-id="f5b35-108">Some controls, like a group box, are merely a simple container of other controls.</span></span> <span data-ttu-id="f5b35-109">在這種情況下，簡單的控制項（稱為簡單框架）不需要執行所有的容器需求。</span><span class="sxs-lookup"><span data-stu-id="f5b35-109">In such cases, the simple control, called a simple frame, doesn't have to implement all the container requirements.</span></span> <span data-ttu-id="f5b35-110">它可以將大部分的介面呼叫從其包含的控制項委派給管理簡單框架的容器。</span><span class="sxs-lookup"><span data-stu-id="f5b35-110">It can delegate most of the interface calls from its contained controls to the container that manages the simple frame.</span></span> <span data-ttu-id="f5b35-111">除了介面呼叫之外，簡單框架也必須處理可能來自其中控制項的 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="f5b35-111">Besides interface calls, the simple frame also has to deal with Windows messages that potentially come from controls within it.</span></span> <span data-ttu-id="f5b35-112">基於這個理由，容器會提供 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) ，以允許這類簡單的框架控制項將訊息傳遞至容器。</span><span class="sxs-lookup"><span data-stu-id="f5b35-112">For this reason, a container supplies [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) to allow such simple frame controls to pass messages up to the container.</span></span> <span data-ttu-id="f5b35-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) 會先處理訊息;在簡單框架處理訊息本身之後，會呼叫 [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) 。</span><span class="sxs-lookup"><span data-stu-id="f5b35-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processes the message first; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) is called after the simple frame has processed the message itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5b35-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5b35-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5b35-115">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="f5b35-115">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




