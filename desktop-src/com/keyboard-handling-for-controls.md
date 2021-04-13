---
title: 控制項的鍵盤處理
description: 控制項會回應鍵盤快速鍵，讓終端使用者可以起始控制項所執行的動作。
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311402"
---
# <a name="keyboard-handling-for-controls"></a><span data-ttu-id="681c3-103">控制項的鍵盤處理</span><span class="sxs-lookup"><span data-stu-id="681c3-103">Keyboard Handling for Controls</span></span>

<span data-ttu-id="681c3-104">控制項會回應鍵盤快速鍵，讓終端使用者可以起始控制項所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="681c3-104">A control responds to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="681c3-105">容器會管理其所有內嵌控制項的鍵盤活動。</span><span class="sxs-lookup"><span data-stu-id="681c3-105">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="681c3-106">使用複合檔案時，鍵盤快速鍵只會套用至目前作用中的物件。</span><span class="sxs-lookup"><span data-stu-id="681c3-106">With compound documents, keyboard accelerators apply only to the currently active object.</span></span> <span data-ttu-id="681c3-107">使用控制項時，已新增一個機制，讓控制項可以回應其鍵盤助憶鍵，即使它目前不是 UI 作用中也一樣。</span><span class="sxs-lookup"><span data-stu-id="681c3-107">With controls, a mechanism has been added so that a control can respond to its keyboard mnemonics even if it is not currently UI-active.</span></span>

<span data-ttu-id="681c3-108">[**IOleControl：： GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo)和 [**IOleControl：： OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)方法和 [**>iolecontrolsite：： OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged)方法會處理控制項的鍵盤助憶鍵。</span><span class="sxs-lookup"><span data-stu-id="681c3-108">The [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) methods and the [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) method handle a control's keyboard mnemonics.</span></span> <span data-ttu-id="681c3-109">[**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo)結構描述控制項的助憶鍵加速器，而且透過 **GetControlInfo** 方法傳遞給它的旗標會以 Enter 和 Esc 鍵描述控制項行為。</span><span class="sxs-lookup"><span data-stu-id="681c3-109">A [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) structure describes a control's mnemonic accelerators, and the flags passed back with it through the **GetControlInfo** method describe the controls behavior with the Enter and Esc keys.</span></span> <span data-ttu-id="681c3-110">當控制項變更其助憶鍵時，它會呼叫 **OnControlInfoChanged** ，讓容器可以在必要時重載結構。</span><span class="sxs-lookup"><span data-stu-id="681c3-110">When a control changes its mnemonics, it calls **OnControlInfoChanged** so the container can reload the structure if necessary.</span></span>

<span data-ttu-id="681c3-111">當控制項是 UI 作用中時，它也是具有焦點的控制項。</span><span class="sxs-lookup"><span data-stu-id="681c3-111">When a control is UI active, it is also the control with the focus.</span></span> <span data-ttu-id="681c3-112">當控制項在就地作用中和 UI 作用中狀態之間啟用和停用時，控制項會呼叫 [**>iolecontrolsite：： OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) 來告訴容器這類變更。</span><span class="sxs-lookup"><span data-stu-id="681c3-112">As controls are activated and deactivated between the in-place active and the UI active states, the control calls [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) to tell the container of such changes.</span></span>

<span data-ttu-id="681c3-113">此外，當控制項是 UI 作用中時，它會先有機會處理任何擊鍵。</span><span class="sxs-lookup"><span data-stu-id="681c3-113">In addition, when a control is UI active, it will have first chance to process any keystrokes.</span></span> <span data-ttu-id="681c3-114">為了讓容器有機會在控制項之前處理按鍵，控制項會呼叫 [**>iolecontrolsite：： TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)。</span><span class="sxs-lookup"><span data-stu-id="681c3-114">To give a container the opportunity to process the keystroke before the control, the control calls [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span></span> <span data-ttu-id="681c3-115">如果容器沒有處理按鍵，控制項接著會處理它。</span><span class="sxs-lookup"><span data-stu-id="681c3-115">If the container does not handle the keystroke, the control then processes it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="681c3-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="681c3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="681c3-117">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="681c3-117">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




