---
description: GetDVDTextLanguageLCID 方法會針對指定的文字字串區塊，抓取 (LCID) 的地區設定識別碼。
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: GetDVDTextLanguageLCID 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509819"
---
# <a name="getdvdtextlanguagelcid-method"></a><span data-ttu-id="da3a3-103">GetDVDTextLanguageLCID 方法</span><span class="sxs-lookup"><span data-stu-id="da3a3-103">GetDVDTextLanguageLCID Method</span></span>

> [!Note]  
> <span data-ttu-id="da3a3-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="da3a3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="da3a3-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="da3a3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="da3a3-106">`GetDVDTextLanguageLCID`方法會針對指定的文字字串區塊，抓取 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="da3a3-106">The `GetDVDTextLanguageLCID` method retrieves the locale identifier (LCID) for the specified text string block.</span></span>

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="da3a3-107">參數</span><span class="sxs-lookup"><span data-stu-id="da3a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da3a3-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="da3a3-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="da3a3-109">將光碟上的文字語言區塊指定為整數。</span><span class="sxs-lookup"><span data-stu-id="da3a3-109">Specifies the text language block on the disc as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da3a3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="da3a3-110">Return Value</span></span>

<span data-ttu-id="da3a3-111">傳回 LCID 值，其中包含指定撰寫字串時所使用之語言的資訊。</span><span class="sxs-lookup"><span data-stu-id="da3a3-111">Returns an LCID value that contains information specifying the language the strings are written in.</span></span>

## <a name="remarks"></a><span data-ttu-id="da3a3-112">備註</span><span class="sxs-lookup"><span data-stu-id="da3a3-112">Remarks</span></span>

<span data-ttu-id="da3a3-113">補充文字字串會儲存在光碟的連續區塊中。每種語言都有一個字串區塊。</span><span class="sxs-lookup"><span data-stu-id="da3a3-113">Supplemental text strings are stored in contiguous blocks on the disc. Each language has one block of strings.</span></span> <span data-ttu-id="da3a3-114">應用程式會以索引指定這些區塊，而索引必須小於 [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md)傳回的值。</span><span class="sxs-lookup"><span data-stu-id="da3a3-114">An application specifies these blocks by an index, which must be less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="da3a3-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da3a3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3a3-116">MSWebDVD 物件</span><span class="sxs-lookup"><span data-stu-id="da3a3-116">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> <dt>

[<span data-ttu-id="da3a3-117">**GetLangFromLangID**</span><span class="sxs-lookup"><span data-stu-id="da3a3-117">**GetLangFromLangID**</span></span>](getlangfromlangid-method.md)
</dt> </dl>

 

 



