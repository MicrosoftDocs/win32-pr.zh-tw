---
description: GetDVDTextStringType 方法會抓取值，指出指定之 DVD 文字字串中所包含的資訊類型。
ms.assetid: 8e22fa2e-e7eb-4dd8-b365-631986bad03e
title: GetDVDTextStringType 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7205025f1f7269737a4be11639f2f0dfe5e43911
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846579"
---
# <a name="getdvdtextstringtype-method"></a><span data-ttu-id="4f9e6-103">GetDVDTextStringType 方法</span><span class="sxs-lookup"><span data-stu-id="4f9e6-103">GetDVDTextStringType Method</span></span>

> [!Note]  
> <span data-ttu-id="4f9e6-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="4f9e6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4f9e6-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="4f9e6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4f9e6-106">`GetDVDTextStringType`方法會抓取值，指出指定之 DVD 文字字串中所包含的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="4f9e6-106">The `GetDVDTextStringType` method retrieves a value that indicates the type of information contained in the specified DVD text string.</span></span>

``` syntax
[ iStringType = ] MSWebDVD.GetDVDTextStringType(iLangIndex, iStringIndex)
```

## <a name="parameters"></a><span data-ttu-id="4f9e6-107">參數</span><span class="sxs-lookup"><span data-stu-id="4f9e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f9e6-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="4f9e6-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="4f9e6-109">將文字字串的語言指定為整數。</span><span class="sxs-lookup"><span data-stu-id="4f9e6-109">Specifies the language of the text string as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="4f9e6-110"><span id="iStringIndex"></span><span id="istringindex"></span><span id="ISTRINGINDEX"></span>*iStringIndex*</span><span class="sxs-lookup"><span data-stu-id="4f9e6-110"><span id="iStringIndex"></span><span id="istringindex"></span><span id="ISTRINGINDEX"></span>*iStringIndex*</span></span>
</dt> <dd>

<span data-ttu-id="4f9e6-111">將文字字串的索引編號指定為整數。</span><span class="sxs-lookup"><span data-stu-id="4f9e6-111">Specifies the index number of the text string as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f9e6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f9e6-112">Return Value</span></span>

<span data-ttu-id="4f9e6-113">傳回整數值，這個值表示字串中所包含的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="4f9e6-113">Returns an integer value that indicates the type of information contained in the string.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f9e6-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f9e6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9e6-115">MSWebDVD 物件</span><span class="sxs-lookup"><span data-stu-id="4f9e6-115">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



