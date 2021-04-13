---
description: SelectParentalLevel 方法會設定指定的家長層級，以供後續播放之用。
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: SelectParentalLevel 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509979"
---
# <a name="selectparentallevel-method"></a><span data-ttu-id="fcb1e-103">SelectParentalLevel 方法</span><span class="sxs-lookup"><span data-stu-id="fcb1e-103">SelectParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="fcb1e-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fcb1e-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fcb1e-106">`SelectParentalLevel`方法會設定指定的家長層級，以供後續播放之用。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-106">The `SelectParentalLevel` method sets the specified parental level for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="fcb1e-107">參數</span><span class="sxs-lookup"><span data-stu-id="fcb1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcb1e-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="fcb1e-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="fcb1e-109">將家長管理層級指定為整數。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-109">Specifies the parental management level as an Integer.</span></span> <span data-ttu-id="fcb1e-110">若要啟用家長管理， *iLevel* 參數的範圍必須介於1到8之間。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-110">To enable the parental management, the *iLevel* parameter must range from 1 through 8.</span></span> <span data-ttu-id="fcb1e-111">若要停用家長管理，請將 *iLevel* 設定為-1。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-111">To disable the parental management, set *iLevel* to -1.</span></span>

</dd> <dt>

<span data-ttu-id="fcb1e-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="fcb1e-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="fcb1e-113">將目前使用者指定為字串。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-113">Specifies the current user as a String.</span></span> <span data-ttu-id="fcb1e-114"> (目前已忽略。 ) </span><span class="sxs-lookup"><span data-stu-id="fcb1e-114">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="fcb1e-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="fcb1e-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="fcb1e-116">將目前儲存在登錄中的密碼指定為字串。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-116">Specifies the password currently stored in the registry as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcb1e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcb1e-117">Return Value</span></span>

<span data-ttu-id="fcb1e-118">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb1e-119">備註</span><span class="sxs-lookup"><span data-stu-id="fcb1e-119">Remarks</span></span>

<span data-ttu-id="fcb1e-120">這個方法會設定 MSWebDVD 物件中的存取層級，以決定使用者可播放的內容。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-120">This method sets the access level in the MSWebDVD object, which determines what content the user can play back.</span></span> <span data-ttu-id="fcb1e-121">較高層級可以播放較低層級的內容，但較低層級無法播放較高層級的內容。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-121">Higher levels can play lower-level content but lower levels can't play higher-level content.</span></span> <span data-ttu-id="fcb1e-122">八個 DVD 家長監護管理層級的確切意義會根據國家/地區而有所不同。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-122">The exact meaning of the eight DVD parental management levels varies depending on the country/region.</span></span> <span data-ttu-id="fcb1e-123">在美國和加拿大地區，這些層級會對應至北美洲的「運動圖片」關聯 (MPAA) 評等類別。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-123">In the United States and Canada, the levels are mapped to the Motion Picture Association of America (MPAA) rating categories.</span></span> <span data-ttu-id="fcb1e-124">預設會停用 [DVD 瀏覽器] 中的 [家長管理]。</span><span class="sxs-lookup"><span data-stu-id="fcb1e-124">Parental management in the DVD Navigator is disabled by default.</span></span>

## <a name="see-also"></a><span data-ttu-id="fcb1e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcb1e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb1e-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="fcb1e-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="fcb1e-127">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="fcb1e-127">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="fcb1e-128">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="fcb1e-128">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="fcb1e-129">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="fcb1e-129">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="fcb1e-130">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="fcb1e-130">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="fcb1e-131">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="fcb1e-131">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



