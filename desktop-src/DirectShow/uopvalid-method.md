---
description: UOPValid 方法會抓取值，指出指定的使用者作業 (UOP) 目前是否有效。
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: 'UOPValid 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984301"
---
# <a name="uopvalid-method"></a><span data-ttu-id="0c381-103">UOPValid 方法</span><span class="sxs-lookup"><span data-stu-id="0c381-103">UOPValid Method</span></span>

> [!Note]  
> <span data-ttu-id="0c381-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="0c381-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0c381-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0c381-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0c381-106">`UOPValid`方法會抓取值，指出指定的使用者作業 (UOP) 目前是否有效。</span><span class="sxs-lookup"><span data-stu-id="0c381-106">The `UOPValid` method retrieves a value that indicates whether the specified user operation (UOP) is currently valid.</span></span>

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a><span data-ttu-id="0c381-107">參數</span><span class="sxs-lookup"><span data-stu-id="0c381-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c381-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span><span class="sxs-lookup"><span data-stu-id="0c381-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span></span>
</dt> <dd>

<span data-ttu-id="0c381-109">指定使用者作業 (UOP) 為整數。</span><span class="sxs-lookup"><span data-stu-id="0c381-109">Specifies the user operation (UOP) as an Integer.</span></span>



| <span data-ttu-id="0c381-110">值</span><span class="sxs-lookup"><span data-stu-id="0c381-110">Value</span></span> | <span data-ttu-id="0c381-111">描述</span><span class="sxs-lookup"><span data-stu-id="0c381-111">Description</span></span>                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c381-112">0</span><span class="sxs-lookup"><span data-stu-id="0c381-112">0</span></span>     | <span data-ttu-id="0c381-113">[**PlayTitle**](playtitle-method.md)、 [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span><span class="sxs-lookup"><span data-stu-id="0c381-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span></span>                                                                                      |
| <span data-ttu-id="0c381-114">1</span><span class="sxs-lookup"><span data-stu-id="0c381-114">1</span></span>     | [<span data-ttu-id="0c381-115">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="0c381-115">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="0c381-116">2</span><span class="sxs-lookup"><span data-stu-id="0c381-116">2</span></span>     | [<span data-ttu-id="0c381-117">**PlayTitle**</span><span class="sxs-lookup"><span data-stu-id="0c381-117">**PlayTitle**</span></span>](playtitle-method.md)                                                                                                                                                                                    |
| <span data-ttu-id="0c381-118">3</span><span class="sxs-lookup"><span data-stu-id="0c381-118">3</span></span>     | [<span data-ttu-id="0c381-119">**停止**</span><span class="sxs-lookup"><span data-stu-id="0c381-119">**Stop**</span></span>](stop-method.md)                                                                                                                                                                                              |
| <span data-ttu-id="0c381-120">4</span><span class="sxs-lookup"><span data-stu-id="0c381-120">4</span></span>     | [<span data-ttu-id="0c381-121">**ReturnFromSubmenu**</span><span class="sxs-lookup"><span data-stu-id="0c381-121">**ReturnFromSubmenu**</span></span>](returnfromsubmenu-method.md)                                                                                                                                                                    |
| <span data-ttu-id="0c381-122">5</span><span class="sxs-lookup"><span data-stu-id="0c381-122">5</span></span>     | [<span data-ttu-id="0c381-123">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="0c381-123">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="0c381-124">6</span><span class="sxs-lookup"><span data-stu-id="0c381-124">6</span></span>     | <span data-ttu-id="0c381-125">[**PlayPrevChapter**](playprevchapter-method.md)、 [ **ReplayChapter**](replaychapter-method.md)</span><span class="sxs-lookup"><span data-stu-id="0c381-125">[**PlayPrevChapter**](playprevchapter-method.md), [**ReplayChapter**](replaychapter-method.md)</span></span>                                                                                                                         |
| <span data-ttu-id="0c381-126">7</span><span class="sxs-lookup"><span data-stu-id="0c381-126">7</span></span>     | [<span data-ttu-id="0c381-127">**PlayNextChapter**</span><span class="sxs-lookup"><span data-stu-id="0c381-127">**PlayNextChapter**</span></span>](playnextchapter-method.md)                                                                                                                                                                        |
| <span data-ttu-id="0c381-128">8</span><span class="sxs-lookup"><span data-stu-id="0c381-128">8</span></span>     | [<span data-ttu-id="0c381-129">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="0c381-129">**PlayForwards**</span></span>](playforwards-method.md)                                                                                                                                                                              |
| <span data-ttu-id="0c381-130">9</span><span class="sxs-lookup"><span data-stu-id="0c381-130">9</span></span>     | [<span data-ttu-id="0c381-131">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="0c381-131">**PlayBackwards**</span></span>](playbackwards-method.md)                                                                                                                                                                            |
| <span data-ttu-id="0c381-132">10</span><span class="sxs-lookup"><span data-stu-id="0c381-132">10</span></span>    | <span data-ttu-id="0c381-133">[](showmenu-method.md)參數值為 2 (DVD \_ 功能表標題的 ShowMenu \_) </span><span class="sxs-lookup"><span data-stu-id="0c381-133">[**ShowMenu**](showmenu-method.md) with a parameter value of 2 (DVD\_MENU\_Title)</span></span>                                                                                                                                       |
| <span data-ttu-id="0c381-134">11</span><span class="sxs-lookup"><span data-stu-id="0c381-134">11</span></span>    | <span data-ttu-id="0c381-135">[](showmenu-method.md)參數值為 3 (DVD \_ 功能表 \_ 根目錄) 的 ShowMenu</span><span class="sxs-lookup"><span data-stu-id="0c381-135">[**ShowMenu**](showmenu-method.md) with a parameter value of 3 (DVD\_MENU\_Root)</span></span>                                                                                                                                        |
| <span data-ttu-id="0c381-136">12</span><span class="sxs-lookup"><span data-stu-id="0c381-136">12</span></span>    | <span data-ttu-id="0c381-137">[](showmenu-method.md)參數值為 4 (DVD \_ 功能表子圖片的 ShowMenu \_) </span><span class="sxs-lookup"><span data-stu-id="0c381-137">[**ShowMenu**](showmenu-method.md) with a parameter value of 4 (DVD\_MENU\_Subpicture)</span></span>                                                                                                                                  |
| <span data-ttu-id="0c381-138">13</span><span class="sxs-lookup"><span data-stu-id="0c381-138">13</span></span>    | <span data-ttu-id="0c381-139">[](showmenu-method.md)參數值為 5 (DVD \_ 功能表 \_ 音訊) 的 ShowMenu</span><span class="sxs-lookup"><span data-stu-id="0c381-139">[**ShowMenu**](showmenu-method.md) with a parameter value of 5 (DVD\_MENU\_Audio)</span></span>                                                                                                                                       |
| <span data-ttu-id="0c381-140">14</span><span class="sxs-lookup"><span data-stu-id="0c381-140">14</span></span>    | <span data-ttu-id="0c381-141">[](showmenu-method.md)參數值為 6 (DVD \_ 功能表角度的 ShowMenu \_) </span><span class="sxs-lookup"><span data-stu-id="0c381-141">[**ShowMenu**](showmenu-method.md) with a parameter value of 6 (DVD\_MENU\_Angle)</span></span>                                                                                                                                       |
| <span data-ttu-id="0c381-142">15</span><span class="sxs-lookup"><span data-stu-id="0c381-142">15</span></span>    | <span data-ttu-id="0c381-143">[](showmenu-method.md)參數值為 7 (DVD \_ 功能表章節的 ShowMenu \_) </span><span class="sxs-lookup"><span data-stu-id="0c381-143">[**ShowMenu**](showmenu-method.md) with a parameter value of 7 (DVD\_MENU\_Chapter)</span></span>                                                                                                                                     |
| <span data-ttu-id="0c381-144">16</span><span class="sxs-lookup"><span data-stu-id="0c381-144">16</span></span>    | [<span data-ttu-id="0c381-145">**繼續**</span><span class="sxs-lookup"><span data-stu-id="0c381-145">**Resume**</span></span>](resume-method.md)                                                                                                                                                                                          |
| <span data-ttu-id="0c381-146">17</span><span class="sxs-lookup"><span data-stu-id="0c381-146">17</span></span>    | <span data-ttu-id="0c381-147">[**SelectLeftButton**](selectleftbutton-method.md)、 [**SelectRightButton**](selectrightbutton-method.md)、 [**SelectUpperButton**](selectupperbutton-method.md)、 [**SelectLowerButton**](selectlowerbutton-method.md)</span><span class="sxs-lookup"><span data-stu-id="0c381-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span></span> |
| <span data-ttu-id="0c381-148">18</span><span class="sxs-lookup"><span data-stu-id="0c381-148">18</span></span>    | [<span data-ttu-id="0c381-149">**StillOff**</span><span class="sxs-lookup"><span data-stu-id="0c381-149">**StillOff**</span></span>](stilloff-method.md)                                                                                                                                                                                      |
| <span data-ttu-id="0c381-150">19</span><span class="sxs-lookup"><span data-stu-id="0c381-150">19</span></span>    | [<span data-ttu-id="0c381-151">**暫停**</span><span class="sxs-lookup"><span data-stu-id="0c381-151">**Pause**</span></span>](pause-method.md)                                                                                                                                                                                            |
| <span data-ttu-id="0c381-152">20</span><span class="sxs-lookup"><span data-stu-id="0c381-152">20</span></span>    | [<span data-ttu-id="0c381-153">**CurrentAudioStream**</span><span class="sxs-lookup"><span data-stu-id="0c381-153">**CurrentAudioStream**</span></span>](currentaudiostream-property.md)                                                                                                                                                                |
| <span data-ttu-id="0c381-154">21</span><span class="sxs-lookup"><span data-stu-id="0c381-154">21</span></span>    | [<span data-ttu-id="0c381-155">**CurrentSubpictureStream**</span><span class="sxs-lookup"><span data-stu-id="0c381-155">**CurrentSubpictureStream**</span></span>](currentsubpicturestream-property.md)                                                                                                                                                      |
| <span data-ttu-id="0c381-156">22</span><span class="sxs-lookup"><span data-stu-id="0c381-156">22</span></span>    | <span data-ttu-id="0c381-157">[**CurrentAngle**](currentangle-property.md)、 [ **SelectParentalLevel**](selectparentallevel-method.md)</span><span class="sxs-lookup"><span data-stu-id="0c381-157">[**CurrentAngle**](currentangle-property.md), [**SelectParentalLevel**](selectparentallevel-method.md)</span></span>                                                                                                                 |
| <span data-ttu-id="0c381-158">23</span><span class="sxs-lookup"><span data-stu-id="0c381-158">23</span></span>    | [<span data-ttu-id="0c381-159">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="0c381-159">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| <span data-ttu-id="0c381-160">24</span><span class="sxs-lookup"><span data-stu-id="0c381-160">24</span></span>    | <span data-ttu-id="0c381-161">選取影片模式喜好設定。</span><span class="sxs-lookup"><span data-stu-id="0c381-161">Select video mode preference.</span></span>                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c381-162">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c381-162">Return Value</span></span>

<span data-ttu-id="0c381-163">傳回布林值，指出 UOP 控制項是否允許指定的作業。</span><span class="sxs-lookup"><span data-stu-id="0c381-163">Returns a Boolean value indicating whether the specified operation is permitted by UOP control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c381-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c381-164">Requirements</span></span>



| <span data-ttu-id="0c381-165">需求</span><span class="sxs-lookup"><span data-stu-id="0c381-165">Requirement</span></span> | <span data-ttu-id="0c381-166">值</span><span class="sxs-lookup"><span data-stu-id="0c381-166">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c381-167">標頭</span><span class="sxs-lookup"><span data-stu-id="0c381-167">Header</span></span><br/> | <dl> <span data-ttu-id="0c381-168"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c381-168"><dt>Segment.h</dt></span></span> </dl> |



 

 




