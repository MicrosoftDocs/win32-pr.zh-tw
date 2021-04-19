---
description: DVDAdm. SaveParentalCountry 方法會將應用程式的新家長/區域儲存至登錄。
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: 'SaveParentalCountry 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982632"
---
# <a name="saveparentalcountry-method"></a><span data-ttu-id="f8b97-103">SaveParentalCountry 方法</span><span class="sxs-lookup"><span data-stu-id="f8b97-103">SaveParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="f8b97-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f8b97-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f8b97-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f8b97-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f8b97-106">方法會將 `DVDAdm.SaveParentalCountry` 應用程式的新家長/區域儲存至登錄。</span><span class="sxs-lookup"><span data-stu-id="f8b97-106">The `DVDAdm.SaveParentalCountry` method saves the application's new parental country/region to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="f8b97-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8b97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b97-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="f8b97-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="f8b97-109">將家長的國家/地區指定為整數。</span><span class="sxs-lookup"><span data-stu-id="f8b97-109">Specifies the parental country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="f8b97-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="f8b97-111">將使用者名稱指定為字串。</span><span class="sxs-lookup"><span data-stu-id="f8b97-111">Specifies the user name as a String.</span></span> <span data-ttu-id="f8b97-112"> (目前已忽略。 ) </span><span class="sxs-lookup"><span data-stu-id="f8b97-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="f8b97-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="f8b97-114">將密碼指定為字串。</span><span class="sxs-lookup"><span data-stu-id="f8b97-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b97-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8b97-115">Return value</span></span>

<span data-ttu-id="f8b97-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f8b97-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b97-117">備註</span><span class="sxs-lookup"><span data-stu-id="f8b97-117">Remarks</span></span>

<span data-ttu-id="f8b97-118">此方法可讓知道目前密碼的使用者將新的家長監護/區域設定儲存至登錄。</span><span class="sxs-lookup"><span data-stu-id="f8b97-118">This method enables a user who knows the current password to save a new parental country/region setting to the registry.</span></span> <span data-ttu-id="f8b97-119">如同 **MSDVDAdm** 的所有方法，這個方法不會影響播放程式中目前的層級;它只會變更登錄設定，以便下一次建立 MSWebDVD 物件時，會以新的國家/地區開啟。</span><span class="sxs-lookup"><span data-stu-id="f8b97-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is created, it will open with the new country/region.</span></span> <span data-ttu-id="f8b97-120">若要在 player 中變更家長監護/區域，請呼叫 [**SelectParentalCountry**](selectparentalcountry-method.md)，而不會變更登錄設定。</span><span class="sxs-lookup"><span data-stu-id="f8b97-120">To change the parental country/region in the player, call [**SelectParentalCountry**](selectparentalcountry-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b97-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8b97-121">Requirements</span></span>



| <span data-ttu-id="f8b97-122">需求</span><span class="sxs-lookup"><span data-stu-id="f8b97-122">Requirement</span></span> | <span data-ttu-id="f8b97-123">值</span><span class="sxs-lookup"><span data-stu-id="f8b97-123">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b97-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f8b97-124">Header</span></span><br/> | <dl> <span data-ttu-id="f8b97-125"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-125"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b97-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8b97-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b97-127">**SaveParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="f8b97-127">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="f8b97-128">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="f8b97-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




