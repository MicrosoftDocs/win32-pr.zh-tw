---
title: '屬性 (IInertiaProcessor) '
description: 此區段包含 IInertiaProcessor 介面的屬性。
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Touch，IInertiaProcessor 介面
- Windows Touch，介面屬性
- 慣性、IInertiaProcessor 介面
- IInertiaProcessor 介面，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab3e1754c7b723b4be446e82fd0ba39fc67af5d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383514"
---
# <a name="properties-iinertiaprocessor"></a><span data-ttu-id="f736e-107">屬性 (IInertiaProcessor) </span><span class="sxs-lookup"><span data-stu-id="f736e-107">Properties (IInertiaProcessor)</span></span>

<span data-ttu-id="f736e-108">此區段包含 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="f736e-108">This section contains the properties for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="f736e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f736e-109">Property</span></span>                                                                               | <span data-ttu-id="f736e-110">描述</span><span class="sxs-lookup"><span data-stu-id="f736e-110">Desription</span></span>                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f736e-111">**InitialOriginX**</span><span class="sxs-lookup"><span data-stu-id="f736e-111">**InitialOriginX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | <span data-ttu-id="f736e-112">使用 intertia 指定目標的起始水準位置。</span><span class="sxs-lookup"><span data-stu-id="f736e-112">Specifies the starting horizontal location for a target with intertia.</span></span>                                   |
| [<span data-ttu-id="f736e-113">**InitialOriginY**</span><span class="sxs-lookup"><span data-stu-id="f736e-113">**InitialOriginY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | <span data-ttu-id="f736e-114">使用 intertia 指定目標的開始垂直位置。</span><span class="sxs-lookup"><span data-stu-id="f736e-114">Specifies the starting vertical location for a target with intertia.</span></span>                                     |
| [<span data-ttu-id="f736e-115">**InitialVelocityX**</span><span class="sxs-lookup"><span data-stu-id="f736e-115">**InitialVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | <span data-ttu-id="f736e-116">指定水準軸上目標物件的初始移動。</span><span class="sxs-lookup"><span data-stu-id="f736e-116">Specifies the initial movement of the target object on the horizontal axis.</span></span>                              |
| [<span data-ttu-id="f736e-117">**InitialVelocityY**</span><span class="sxs-lookup"><span data-stu-id="f736e-117">**InitialVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | <span data-ttu-id="f736e-118">指定垂直軸上目標物件的初始移動。</span><span class="sxs-lookup"><span data-stu-id="f736e-118">Specifies the initial movement of the target object on the vertical axis.</span></span>                                |
| [<span data-ttu-id="f736e-119">**InitialAngularVelocity**</span><span class="sxs-lookup"><span data-stu-id="f736e-119">**InitialAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | <span data-ttu-id="f736e-120">指定開始移動時目標的旋轉速度。</span><span class="sxs-lookup"><span data-stu-id="f736e-120">Specifies the rotational velocity of the target when movement begins.</span></span>                                    |
| [<span data-ttu-id="f736e-121">**InitialExpansionVelocity**</span><span class="sxs-lookup"><span data-stu-id="f736e-121">**InitialExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | <span data-ttu-id="f736e-122">指定移動開始時，目標的 radius 擴充速率。</span><span class="sxs-lookup"><span data-stu-id="f736e-122">Specifies the rate of radius expansion of the target when movement begins.</span></span>                               |
| [<span data-ttu-id="f736e-123">**InitialRadius**</span><span class="sxs-lookup"><span data-stu-id="f736e-123">**InitialRadius**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | <span data-ttu-id="f736e-124">指定在物件變更之前，從目標邊緣到其中心的距離。</span><span class="sxs-lookup"><span data-stu-id="f736e-124">Specifies the distance from the edge of the target to its center before the object was changed.</span></span>          |
| [<span data-ttu-id="f736e-125">**BoundaryLeft**</span><span class="sxs-lookup"><span data-stu-id="f736e-125">**BoundaryLeft**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | <span data-ttu-id="f736e-126">限制目標物件可以移動到螢幕左邊的距離。</span><span class="sxs-lookup"><span data-stu-id="f736e-126">Limits how far toward the left of the screen the target object can move.</span></span>                                 |
| [<span data-ttu-id="f736e-127">**BoundaryTop**</span><span class="sxs-lookup"><span data-stu-id="f736e-127">**BoundaryTop**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | <span data-ttu-id="f736e-128">限制目標物件可以移動到螢幕頂端的距離。</span><span class="sxs-lookup"><span data-stu-id="f736e-128">Limits how far toward the top of the screen the target object can move.</span></span>                                  |
| [<span data-ttu-id="f736e-129">**BoundaryRight**</span><span class="sxs-lookup"><span data-stu-id="f736e-129">**BoundaryRight**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | <span data-ttu-id="f736e-130">限制目標物件可以移動到畫面右邊的距離。</span><span class="sxs-lookup"><span data-stu-id="f736e-130">Limits how far toward the right side of the screen the target object can move.</span></span>                           |
| [<span data-ttu-id="f736e-131">**BoundaryBottom**</span><span class="sxs-lookup"><span data-stu-id="f736e-131">**BoundaryBottom**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | <span data-ttu-id="f736e-132">限制目標物件可以移動到畫面底部的距離。</span><span class="sxs-lookup"><span data-stu-id="f736e-132">Limits how far toward the bottom of the screen the target object can move.</span></span>                               |
| [<span data-ttu-id="f736e-133">**ElasticMarginLeft**</span><span class="sxs-lookup"><span data-stu-id="f736e-133">**ElasticMarginLeft**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | <span data-ttu-id="f736e-134">指定跳動目標物件的最左邊區域。</span><span class="sxs-lookup"><span data-stu-id="f736e-134">Specifies the leftmost region for bouncing the target object.</span></span>                                            |
| [<span data-ttu-id="f736e-135">**ElasticMarginTop**</span><span class="sxs-lookup"><span data-stu-id="f736e-135">**ElasticMarginTop**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | <span data-ttu-id="f736e-136">指定跳動目標物件的最上層區域。</span><span class="sxs-lookup"><span data-stu-id="f736e-136">Specifies the topmost region for bouncing the target object.</span></span>                                             |
| [<span data-ttu-id="f736e-137">**ElasticMarginRight**</span><span class="sxs-lookup"><span data-stu-id="f736e-137">**ElasticMarginRight**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | <span data-ttu-id="f736e-138">指定跳動目標物件的最右側區域。</span><span class="sxs-lookup"><span data-stu-id="f736e-138">Specifies the rightmost region for bouncing the target object.</span></span>                                           |
| [<span data-ttu-id="f736e-139">**ElasticMarginBottom**</span><span class="sxs-lookup"><span data-stu-id="f736e-139">**ElasticMarginBottom**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | <span data-ttu-id="f736e-140">指定跳動目標物件的底部區域。</span><span class="sxs-lookup"><span data-stu-id="f736e-140">Specifies the bottom region for bouncing the target object.</span></span>                                              |
| [<span data-ttu-id="f736e-141">**DesiredAngularDeceleration**</span><span class="sxs-lookup"><span data-stu-id="f736e-141">**DesiredAngularDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | <span data-ttu-id="f736e-142">指定目標物件將停止旋轉的預期速率（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="f736e-142">Specifies the desired rate that the target object will stop spinning in radians per msec.</span></span>                |
| [<span data-ttu-id="f736e-143">**DesiredRotation**</span><span class="sxs-lookup"><span data-stu-id="f736e-143">**DesiredRotation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | <span data-ttu-id="f736e-144">以弧度為單位指定所需的距離 () ，慣性處理器會操控物件。</span><span class="sxs-lookup"><span data-stu-id="f736e-144">Specifies the desired distance (in radians) that an object will be manipulated by the inertia processor.</span></span> |
| [<span data-ttu-id="f736e-145">**DesiredExpansion**</span><span class="sxs-lookup"><span data-stu-id="f736e-145">**DesiredExpansion**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | <span data-ttu-id="f736e-146">在物件的平均半徑中指定所需的變更。</span><span class="sxs-lookup"><span data-stu-id="f736e-146">Specifies the desired change in the average radius of the object.</span></span>                                        |
| [<span data-ttu-id="f736e-147">**DesiredExpansionDeceleration**</span><span class="sxs-lookup"><span data-stu-id="f736e-147">**DesiredExpansionDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | <span data-ttu-id="f736e-148">指定物件將停止擴充的速率。</span><span class="sxs-lookup"><span data-stu-id="f736e-148">Specifies the rate at which the object will stop expanding.</span></span>                                              |
| [<span data-ttu-id="f736e-149">**DesiredDeceleration**</span><span class="sxs-lookup"><span data-stu-id="f736e-149">**DesiredDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | <span data-ttu-id="f736e-150">指定轉譯作業將減速的預期速率。</span><span class="sxs-lookup"><span data-stu-id="f736e-150">Specifies the desired rate at which translation operations will decelerate.</span></span>                              |
| [<span data-ttu-id="f736e-151">**DesiredDisplacement**</span><span class="sxs-lookup"><span data-stu-id="f736e-151">**DesiredDisplacement**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | <span data-ttu-id="f736e-152">指定物件將行進的所需距離。</span><span class="sxs-lookup"><span data-stu-id="f736e-152">Specifies the desired distance that the object will travel.</span></span>                                              |
| [<span data-ttu-id="f736e-153">**InitialTimestamp**</span><span class="sxs-lookup"><span data-stu-id="f736e-153">**InitialTimestamp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | <span data-ttu-id="f736e-154">指定具有慣性之目標物件的開始時間戳。</span><span class="sxs-lookup"><span data-stu-id="f736e-154">Specifies the starting time stamp for a target object that has inertia.</span></span>                                  |



 

## <a name="related-topics"></a><span data-ttu-id="f736e-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="f736e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f736e-156">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="f736e-156">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




