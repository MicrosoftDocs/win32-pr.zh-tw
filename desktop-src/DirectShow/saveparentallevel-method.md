---
description: DVDAdm. SaveParentalLevel 方法會將新的預設家長監護儲存至登錄。
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: 'SaveParentalLevel 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976095"
---
# <a name="saveparentallevel-method"></a><span data-ttu-id="61a85-103">SaveParentalLevel 方法</span><span class="sxs-lookup"><span data-stu-id="61a85-103">SaveParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="61a85-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="61a85-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="61a85-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="61a85-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="61a85-106">**DVDAdm. SaveParentalLevel** 方法會將新的預設家長監護儲存至登錄。</span><span class="sxs-lookup"><span data-stu-id="61a85-106">The **DVDAdm.SaveParentalLevel** method saves a new default parental level to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="61a85-107">參數</span><span class="sxs-lookup"><span data-stu-id="61a85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a85-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="61a85-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="61a85-109">將家長層級指定為從1到8的 anInteger 值。</span><span class="sxs-lookup"><span data-stu-id="61a85-109">Specifies the parental level as anInteger value from 1 through 8.</span></span>

</dd> <dt>

<span data-ttu-id="61a85-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="61a85-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="61a85-111">將使用者名稱指定為字串。</span><span class="sxs-lookup"><span data-stu-id="61a85-111">Specifies the user name as a String.</span></span> <span data-ttu-id="61a85-112"> (目前已忽略。 ) </span><span class="sxs-lookup"><span data-stu-id="61a85-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="61a85-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="61a85-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="61a85-114">將密碼指定為字串。</span><span class="sxs-lookup"><span data-stu-id="61a85-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a85-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="61a85-115">Return Value</span></span>

<span data-ttu-id="61a85-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="61a85-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a85-117">備註</span><span class="sxs-lookup"><span data-stu-id="61a85-117">Remarks</span></span>

<span data-ttu-id="61a85-118">此方法可讓知道目前密碼的使用者將新的家長監護設定儲存至登錄。</span><span class="sxs-lookup"><span data-stu-id="61a85-118">This method enables a user who knows the current password to save a new parental level setting to the registry.</span></span> <span data-ttu-id="61a85-119">如同 **MSDVDAdm** 的所有方法，這個方法不會影響播放程式中目前的層級;它只會變更登錄設定，如此 MSWebDVD 物件下次啟動時，就會以新的層級開啟。</span><span class="sxs-lookup"><span data-stu-id="61a85-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is started, it will open with the new level.</span></span> <span data-ttu-id="61a85-120">指定-1 可停用家長管理。</span><span class="sxs-lookup"><span data-stu-id="61a85-120">Specify -1 to disable parental management.</span></span> <span data-ttu-id="61a85-121">若要在播放玩家變更家長監護，請呼叫 [**SelectParentalLevel**](selectparentallevel-method.md)，而不會變更登錄設定。</span><span class="sxs-lookup"><span data-stu-id="61a85-121">To change the parental level in the player, call [**SelectParentalLevel**](selectparentallevel-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a85-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="61a85-122">Requirements</span></span>



| <span data-ttu-id="61a85-123">需求</span><span class="sxs-lookup"><span data-stu-id="61a85-123">Requirement</span></span> | <span data-ttu-id="61a85-124">值</span><span class="sxs-lookup"><span data-stu-id="61a85-124">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61a85-125">標頭</span><span class="sxs-lookup"><span data-stu-id="61a85-125">Header</span></span><br/> | <dl> <span data-ttu-id="61a85-126"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="61a85-126"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a85-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61a85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a85-128">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="61a85-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




