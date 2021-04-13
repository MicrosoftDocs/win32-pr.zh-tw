---
description: SelectParentalCountry 方法會設定指定的家長/區域以進行後續播放。
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: SelectParentalCountry 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510206"
---
# <a name="selectparentalcountry-method"></a><span data-ttu-id="5ed26-103">SelectParentalCountry 方法</span><span class="sxs-lookup"><span data-stu-id="5ed26-103">SelectParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="5ed26-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="5ed26-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5ed26-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5ed26-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5ed26-106">`SelectParentalCountry`方法會設定指定的家長/區域以進行後續播放。</span><span class="sxs-lookup"><span data-stu-id="5ed26-106">The `SelectParentalCountry` method sets the specified parental country/region for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="5ed26-107">參數</span><span class="sxs-lookup"><span data-stu-id="5ed26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed26-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="5ed26-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="5ed26-109">將國家/地區指定為整數。</span><span class="sxs-lookup"><span data-stu-id="5ed26-109">Specifies the country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="5ed26-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="5ed26-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="5ed26-111">將目前登入的使用者指定為字串。</span><span class="sxs-lookup"><span data-stu-id="5ed26-111">Specifies the current logged-on user as a String.</span></span> <span data-ttu-id="5ed26-112"> (目前已忽略。 ) </span><span class="sxs-lookup"><span data-stu-id="5ed26-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="5ed26-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="5ed26-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="5ed26-114">指定應用程式密碼字串。</span><span class="sxs-lookup"><span data-stu-id="5ed26-114">Specifies the application password String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed26-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ed26-115">Return Value</span></span>

<span data-ttu-id="5ed26-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5ed26-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ed26-117">備註</span><span class="sxs-lookup"><span data-stu-id="5ed26-117">Remarks</span></span>

<span data-ttu-id="5ed26-118">家長監護/區域會決定如何解讀家長監護。</span><span class="sxs-lookup"><span data-stu-id="5ed26-118">The parental country/region determines how the parental levels are interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ed26-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ed26-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed26-120">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="5ed26-120">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="5ed26-121">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="5ed26-121">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="5ed26-122">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="5ed26-122">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="5ed26-123">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="5ed26-123">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="5ed26-124">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="5ed26-124">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="5ed26-125">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="5ed26-125">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



