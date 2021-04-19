---
description: GetDVDTextNumberOfStrings 方法會抓取指定語言可用的文字字串數目。
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: GetDVDTextNumberOfStrings 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970702"
---
# <a name="getdvdtextnumberofstrings-method"></a><span data-ttu-id="aa3f9-103">GetDVDTextNumberOfStrings 方法</span><span class="sxs-lookup"><span data-stu-id="aa3f9-103">GetDVDTextNumberOfStrings Method</span></span>

> [!Note]  
> <span data-ttu-id="aa3f9-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="aa3f9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="aa3f9-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="aa3f9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="aa3f9-106">方法會抓取 `GetDVDTextNumberOfStrings` 指定語言可用的文字字串數目。</span><span class="sxs-lookup"><span data-stu-id="aa3f9-106">The `GetDVDTextNumberOfStrings` method retrieves the number of text strings available for the specified language.</span></span>

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="aa3f9-107">參數</span><span class="sxs-lookup"><span data-stu-id="aa3f9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa3f9-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="aa3f9-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="aa3f9-109">將語言指定為整數。</span><span class="sxs-lookup"><span data-stu-id="aa3f9-109">Specifies the language as an Integer.</span></span> <span data-ttu-id="aa3f9-110">值的範圍必須介於零到1之間，且小於 [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md)傳回的值。</span><span class="sxs-lookup"><span data-stu-id="aa3f9-110">The value must range from zero through one less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa3f9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa3f9-111">Return Value</span></span>

<span data-ttu-id="aa3f9-112">傳回整數值，指定光碟在指定的語言中包含多少個字串。</span><span class="sxs-lookup"><span data-stu-id="aa3f9-112">Returns an integer value specifying how many strings the disc contains in the specified language.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa3f9-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa3f9-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3f9-114">MSWebDVD 物件</span><span class="sxs-lookup"><span data-stu-id="aa3f9-114">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



