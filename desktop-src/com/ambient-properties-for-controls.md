---
title: 控制項的環境屬性
description: 控制項的環境屬性
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372311"
---
# <a name="ambient-properties-for-controls"></a><span data-ttu-id="a5f3c-103">控制項的環境屬性</span><span class="sxs-lookup"><span data-stu-id="a5f3c-103">Ambient Properties for Controls</span></span>

<span data-ttu-id="a5f3c-104">如果控制項完全支援任何環境屬性，則必須至少遵循下表所述的下列環境屬性（使用標準 dispid）的值。</span><span class="sxs-lookup"><span data-stu-id="a5f3c-104">If a control supports any ambient properties at all, it must at least respect the values of the following ambient properties under the conditions stated in the following table using the standard dispids.</span></span>



| <span data-ttu-id="a5f3c-105">環境屬性</span><span class="sxs-lookup"><span data-stu-id="a5f3c-105">Ambient Property</span></span>            | <span data-ttu-id="a5f3c-106">Dispid</span><span class="sxs-lookup"><span data-stu-id="a5f3c-106">Dispid</span></span>          | <span data-ttu-id="a5f3c-107">使用的批註/條件</span><span class="sxs-lookup"><span data-stu-id="a5f3c-107">Comment/Conditions for Use</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f3c-108">LocaleID</span><span class="sxs-lookup"><span data-stu-id="a5f3c-108">LocaleID</span></span><br/>         | <span data-ttu-id="a5f3c-109">-705</span><span class="sxs-lookup"><span data-stu-id="a5f3c-109">-705</span></span><br/> | <span data-ttu-id="a5f3c-110">如果對控制項的地區設定很重要，例如文字輸出</span><span class="sxs-lookup"><span data-stu-id="a5f3c-110">If Locale is significant to the control, e.g. for text output</span></span><br/>                                                                                                                                                                                                                  |
| <span data-ttu-id="a5f3c-111">UserMode</span><span class="sxs-lookup"><span data-stu-id="a5f3c-111">UserMode</span></span> <br/>        | <span data-ttu-id="a5f3c-112">-709</span><span class="sxs-lookup"><span data-stu-id="a5f3c-112">-709</span></span><br/> | <span data-ttu-id="a5f3c-113">如果控制項在使用者 (設計) 模式和執行模式中的行為不同</span><span class="sxs-lookup"><span data-stu-id="a5f3c-113">If the control behaves differently in user (design) mode and run mode</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="a5f3c-114">UIDead</span><span class="sxs-lookup"><span data-stu-id="a5f3c-114">UIDead</span></span><br/>           | <span data-ttu-id="a5f3c-115">-710</span><span class="sxs-lookup"><span data-stu-id="a5f3c-115">-710</span></span><br/> | <span data-ttu-id="a5f3c-116">如果控制項回應 UI 事件，則應接受此環境屬性</span><span class="sxs-lookup"><span data-stu-id="a5f3c-116">If the control reacts to UI events, then it should honor this ambient property</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="a5f3c-117">ShowGrabHandles</span><span class="sxs-lookup"><span data-stu-id="a5f3c-117">ShowGrabHandles</span></span><br/>  | <span data-ttu-id="a5f3c-118">-711</span><span class="sxs-lookup"><span data-stu-id="a5f3c-118">-711</span></span><br/> | <span data-ttu-id="a5f3c-119">如果控制項支援就地調整本身的大小</span><span class="sxs-lookup"><span data-stu-id="a5f3c-119">If the control support in-place resizing of itself</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="a5f3c-120">ShowHatching</span><span class="sxs-lookup"><span data-stu-id="a5f3c-120">ShowHatching</span></span><br/>     | <span data-ttu-id="a5f3c-121">-712</span><span class="sxs-lookup"><span data-stu-id="a5f3c-121">-712</span></span><br/> | <span data-ttu-id="a5f3c-122">如果控制項支援就地啟用和 UI 啟用</span><span class="sxs-lookup"><span data-stu-id="a5f3c-122">If the control support in-place activation and UI activation</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="a5f3c-123">DisplayAsDefault</span><span class="sxs-lookup"><span data-stu-id="a5f3c-123">DisplayAsDefault</span></span><br/> | <span data-ttu-id="a5f3c-124">-713</span><span class="sxs-lookup"><span data-stu-id="a5f3c-124">-713</span></span><br/> | <span data-ttu-id="a5f3c-125">只有在控制項標示為 OLEMISC \_ ACTSLIKEBUTTON (這表示已提供支援鍵盤助憶鍵，因此 [**IOleControl：： GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) 和 [**IOleControl：： OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) 必須) 執行。</span><span class="sxs-lookup"><span data-stu-id="a5f3c-125">Only if the control is marked OLEMISC\_ACTSLIKEBUTTON (which means that support for keyboard mnemonics is provided, thus [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) must be implemented).</span></span><br/> |



 

<span data-ttu-id="a5f3c-126">如先前所述，使用 ambients 需要 [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)的 [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (做為最小) ，以及 [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite)和 [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)) 的 [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (。</span><span class="sxs-lookup"><span data-stu-id="a5f3c-126">As described previously, use of ambients requires both [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (for [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) as a minimum) as well as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (for [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) and [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span></span>

<span data-ttu-id="a5f3c-127">\_容器不一定會支援 OLEMISC SETCLIENTSITEFIRST 位。</span><span class="sxs-lookup"><span data-stu-id="a5f3c-127">The OLEMISC\_SETCLIENTSITEFIRST bit may not necessarily be supported by a container.</span></span> <span data-ttu-id="a5f3c-128">在這些情況下，控制項必須使用其所需之環境屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="a5f3c-128">In these circumstances, a control must resort to default values for the ambient properties that it requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f3c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5f3c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f3c-130">控制項</span><span class="sxs-lookup"><span data-stu-id="a5f3c-130">Controls</span></span>](controls.md)
</dt> </dl>

 

 





