---
title: 控制項屬性
description: 控制項屬性
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840784"
---
# <a name="control-properties"></a><span data-ttu-id="c5059-103">控制項屬性</span><span class="sxs-lookup"><span data-stu-id="c5059-103">Control Properties</span></span>

<span data-ttu-id="c5059-104">除了由控制項本身定義和執行的屬性之外，ActiveX 控制項技術也包含：</span><span class="sxs-lookup"><span data-stu-id="c5059-104">In addition to properties defined and implemented by the control itself, ActiveX controls technology also involves:</span></span>

<dl> <dt>

<span data-ttu-id="c5059-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>環境屬性</span><span class="sxs-lookup"><span data-stu-id="c5059-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient properties</span></span>
</dt> <dd>

<span data-ttu-id="c5059-106">這些是由容器透過控制項用戶端網站所公開，以提供適用于所有內嵌在容器中之控制項的環境值。</span><span class="sxs-lookup"><span data-stu-id="c5059-106">These are exposed by the container through a control client site to provide environmental values that apply to all controls embedded in the container.</span></span> <span data-ttu-id="c5059-107">例如，容器可以提供預設的背景色彩或控制項可使用的預設字型。</span><span class="sxs-lookup"><span data-stu-id="c5059-107">For example, a container can provide a default background color or a default font that the control can use.</span></span> <span data-ttu-id="c5059-108">環境屬性會透過在容器的網站物件上實作為 **IDispatch** 來公開。</span><span class="sxs-lookup"><span data-stu-id="c5059-108">Ambient properties are exposed through **IDispatch** implemented on a container's site object.</span></span> <span data-ttu-id="c5059-109">當容器的任何環境屬性變更值時，容器會呼叫控制項的 [**IOleControl：： OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5059-109">The container calls the control's [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) method when any of its ambient properties change value.</span></span> <span data-ttu-id="c5059-110">在回應中，控制項可能需要更新自己的內部或視覺狀態以回應。</span><span class="sxs-lookup"><span data-stu-id="c5059-110">In response, a control may need to update its own internal or visual state in response.</span></span> <span data-ttu-id="c5059-111">容器會指出哪些環境屬性以 DISPID 參數變更，或可能傳遞 DISPID \_ 未知，以指出多個環境屬性已變更。</span><span class="sxs-lookup"><span data-stu-id="c5059-111">The container indicates which ambient property changed with the DISPID parameter or may pass DISPID\_UNKNOWN to indicate that multiple ambient properties changed.</span></span>

</dd> <dt>

<span data-ttu-id="c5059-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>擴充屬性</span><span class="sxs-lookup"><span data-stu-id="c5059-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Extended properties</span></span>
</dt> <dd>

<span data-ttu-id="c5059-113">這些實際上是由容器執行，以包裝其包含的控制項，以提供容器管理的屬性，就像是原生控制項屬性一樣。</span><span class="sxs-lookup"><span data-stu-id="c5059-113">These are actually implemented by a container to wrap the controls it contains to provide container-managed properties that appear as if they were native control properties.</span></span> <span data-ttu-id="c5059-114">容器可以匯總控制項，加入擴充屬性來補充或覆寫控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="c5059-114">The container can aggregate the control, adding the extended properties to supplement or override the control's properties.</span></span> <span data-ttu-id="c5059-115">匯總的物件稱為「擴充控制項」。</span><span class="sxs-lookup"><span data-stu-id="c5059-115">The aggregated object is called an extended control.</span></span> <span data-ttu-id="c5059-116">在容器中，擴充控制項會顯示為控制項本身，而擴充屬性則顯示為由控制項公開。</span><span class="sxs-lookup"><span data-stu-id="c5059-116">To the container, the extended control appears as the control itself and extended properties appear to be exposed by the control.</span></span> <span data-ttu-id="c5059-117">容器透過其用戶端網站方法 [**>iolecontrolsite：： GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)支援擴充的控制項。</span><span class="sxs-lookup"><span data-stu-id="c5059-117">The container supports an extended control through its client site method [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span></span> <span data-ttu-id="c5059-118">如果容器支援這項功能， **GetExtendedControl** 方法可讓控制項在網站之間流覽至容器提供的擴充控制項物件。</span><span class="sxs-lookup"><span data-stu-id="c5059-118">The **GetExtendedControl** method allows controls to navigate through the site to the extended control object provided for them by the container, if the container supports this feature.</span></span> <span data-ttu-id="c5059-119">除了控制項通常透過 [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)指定的頁面之外，容器也可以選擇顯示其擴充控制項的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="c5059-119">A container can also choose to show property pages for its extended controls in addition to those pages that a control would normally specify through [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="c5059-120">因此，控制項必須先要求容器顯示內容框架，控制項才會嘗試這麼做。</span><span class="sxs-lookup"><span data-stu-id="c5059-120">Because of this, a control has to ask a container to show a property frame before the control attempts to do so itself.</span></span> <span data-ttu-id="c5059-121">此控制項會呼叫 [**>iolecontrolsite：： ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) 來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="c5059-121">The control calls [**IOleControlSite::ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) to do this.</span></span> <span data-ttu-id="c5059-122">如果容器會執行此函式，則會顯示內容框架本身;如果方法傳回錯誤，控制項可以顯示內容框架。</span><span class="sxs-lookup"><span data-stu-id="c5059-122">If the container implements this function then it shows the property frame itself; if the method returns an error then the control can show the property frame.</span></span>

</dd> </dl>

<span data-ttu-id="c5059-123">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c5059-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c5059-124">標準屬性</span><span class="sxs-lookup"><span data-stu-id="c5059-124">Standard Properties</span></span>](standard-properties.md)
-   [<span data-ttu-id="c5059-125">標準字型物件</span><span class="sxs-lookup"><span data-stu-id="c5059-125">Standard Font Object</span></span>](standard-font-object.md)
-   [<span data-ttu-id="c5059-126">標準圖片物件</span><span class="sxs-lookup"><span data-stu-id="c5059-126">Standard Picture Object</span></span>](standard-picture-object.md)

## <a name="related-topics"></a><span data-ttu-id="c5059-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5059-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5059-128">控制項方法</span><span class="sxs-lookup"><span data-stu-id="c5059-128">Control Methods</span></span>](control-methods.md)
</dt> </dl>

 

 




