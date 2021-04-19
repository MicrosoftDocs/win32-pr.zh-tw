---
description: DVDAdm. GetParentalCountry 方法會抓取最後儲存至登錄的家長監護/區域。
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: 'GetParentalCountry 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997021"
---
# <a name="getparentalcountry-method"></a><span data-ttu-id="7f70c-103">GetParentalCountry 方法</span><span class="sxs-lookup"><span data-stu-id="7f70c-103">GetParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="7f70c-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="7f70c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7f70c-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="7f70c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7f70c-106">`DVDAdm.GetParentalCountry`方法會抓取上次儲存至登錄的家長監護/區域。</span><span class="sxs-lookup"><span data-stu-id="7f70c-106">The `DVDAdm.GetParentalCountry` method retrieves the parental country/region that was last saved to the registry.</span></span>

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a><span data-ttu-id="7f70c-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f70c-107">Return Value</span></span>

<span data-ttu-id="7f70c-108">傳回整數，指出儲存在登錄中的預設國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="7f70c-108">Returns an Integer indicating the default country/region code stored in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f70c-109">備註</span><span class="sxs-lookup"><span data-stu-id="7f70c-109">Remarks</span></span>

<span data-ttu-id="7f70c-110">此方法所抓取的「家長」國家/地區不一定是目前儲存在 MSWebDVD 物件中的相同國家/地區。</span><span class="sxs-lookup"><span data-stu-id="7f70c-110">The parental country/region this method retrieves is not necessarily the same country/region currently stored in the MSWebDVD object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f70c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f70c-111">Requirements</span></span>



| <span data-ttu-id="7f70c-112">需求</span><span class="sxs-lookup"><span data-stu-id="7f70c-112">Requirement</span></span> | <span data-ttu-id="7f70c-113">值</span><span class="sxs-lookup"><span data-stu-id="7f70c-113">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7f70c-114">標頭</span><span class="sxs-lookup"><span data-stu-id="7f70c-114">Header</span></span><br/> | <dl> <span data-ttu-id="7f70c-115"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f70c-115"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f70c-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f70c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f70c-117">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="7f70c-117">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




