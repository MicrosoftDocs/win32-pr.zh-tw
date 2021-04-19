---
description: NotifyParentalLevelChange 方法會啟用或停用暫存家長管理層級命令的事件處理。
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: 'NotifyParentalLevelChange 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000017"
---
# <a name="notifyparentallevelchange-method"></a><span data-ttu-id="468d2-103">NotifyParentalLevelChange 方法</span><span class="sxs-lookup"><span data-stu-id="468d2-103">NotifyParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="468d2-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="468d2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="468d2-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="468d2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="468d2-106">`NotifyParentalLevelChange`方法會啟用或停用暫存家長管理層級命令的事件處理。</span><span class="sxs-lookup"><span data-stu-id="468d2-106">The `NotifyParentalLevelChange` method enables or disables the event handling for temporary parental management level commands.</span></span>

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a><span data-ttu-id="468d2-107">參數</span><span class="sxs-lookup"><span data-stu-id="468d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="468d2-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span><span class="sxs-lookup"><span data-stu-id="468d2-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span></span>
</dt> <dd>

<span data-ttu-id="468d2-109">指定布林值，指出當 MSWebDVD 物件遇到分級高於整個光碟評等的影片區段時，是否要通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="468d2-109">Specifies a Boolean value indicating whether or not the application is notified when the MSWebDVD object encounters video segments with a rating more restrictive than the overall rating for the disc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="468d2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="468d2-110">Return Value</span></span>

<span data-ttu-id="468d2-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="468d2-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="468d2-112">備註</span><span class="sxs-lookup"><span data-stu-id="468d2-112">Remarks</span></span>

<span data-ttu-id="468d2-113">預設會停用家長監護的管理通知。</span><span class="sxs-lookup"><span data-stu-id="468d2-113">Parental management notifications are disabled by default.</span></span> <span data-ttu-id="468d2-114">這表示允許來自光碟的暫存家長命令，但會忽略，而不會中斷光碟的播放。</span><span class="sxs-lookup"><span data-stu-id="468d2-114">This means that temporary parental commands from the disc are allowed but ignored and disc will play without interruption.</span></span> <span data-ttu-id="468d2-115">如果您需要處理來自光碟的臨時家長管理層級命令，請在初始化應用程式期間呼叫此方法。若要在啟用「家長管理」之後加以停用，請使用 false 的引數來呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="468d2-115">Call this method during initialization of your application if you need to handle temporary parental management level commands from the disc. To disable parental management after it is enabled, call this method with an argument of false.</span></span> <span data-ttu-id="468d2-116">如需有關家長管理的詳細資訊，請參閱 [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)。</span><span class="sxs-lookup"><span data-stu-id="468d2-116">For more details on parental management, see [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="468d2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="468d2-117">Requirements</span></span>



| <span data-ttu-id="468d2-118">需求</span><span class="sxs-lookup"><span data-stu-id="468d2-118">Requirement</span></span> | <span data-ttu-id="468d2-119">值</span><span class="sxs-lookup"><span data-stu-id="468d2-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="468d2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="468d2-120">Header</span></span><br/> | <dl> <span data-ttu-id="468d2-121"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="468d2-121"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="468d2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="468d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="468d2-123">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="468d2-123">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="468d2-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="468d2-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="468d2-125">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="468d2-125">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="468d2-126">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="468d2-126">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="468d2-127">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="468d2-127">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




