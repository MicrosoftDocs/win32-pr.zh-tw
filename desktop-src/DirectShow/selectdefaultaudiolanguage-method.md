---
description: SelectDefaultAudioLanguage 方法會設定 MSWebDVD 物件中目前的預設音訊語言。
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: SelectDefaultAudioLanguage 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509980"
---
# <a name="selectdefaultaudiolanguage-method"></a><span data-ttu-id="90339-103">SelectDefaultAudioLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="90339-103">SelectDefaultAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="90339-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="90339-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="90339-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="90339-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="90339-106">`SelectDefaultAudioLanguage`方法會在 MSWebDVD 物件中設定目前的預設音訊語言。</span><span class="sxs-lookup"><span data-stu-id="90339-106">The `SelectDefaultAudioLanguage` method sets the current default audio language in the MSWebDVD object.</span></span>

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a><span data-ttu-id="90339-107">參數</span><span class="sxs-lookup"><span data-stu-id="90339-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90339-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="90339-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="90339-109">將語言指定為整數 LCID 值。</span><span class="sxs-lookup"><span data-stu-id="90339-109">Specifies the language as an Integer LCID value.</span></span>

</dd> <dt>

<span data-ttu-id="90339-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="90339-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="90339-111">將 DVD-音訊語言延伸模組指定為整數值。</span><span class="sxs-lookup"><span data-stu-id="90339-111">Specifies the DVD audio language extension as an integer value.</span></span>



| <span data-ttu-id="90339-112">值</span><span class="sxs-lookup"><span data-stu-id="90339-112">Value</span></span> | <span data-ttu-id="90339-113">描述</span><span class="sxs-lookup"><span data-stu-id="90339-113">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="90339-114">0</span><span class="sxs-lookup"><span data-stu-id="90339-114">0</span></span>     | <span data-ttu-id="90339-115">NotSpecified</span><span class="sxs-lookup"><span data-stu-id="90339-115">NotSpecified</span></span>      |
| <span data-ttu-id="90339-116">1</span><span class="sxs-lookup"><span data-stu-id="90339-116">1</span></span>     | <span data-ttu-id="90339-117">標題</span><span class="sxs-lookup"><span data-stu-id="90339-117">Captions</span></span>          |
| <span data-ttu-id="90339-118">2</span><span class="sxs-lookup"><span data-stu-id="90339-118">2</span></span>     | <span data-ttu-id="90339-119">VisuallyImpaired</span><span class="sxs-lookup"><span data-stu-id="90339-119">VisuallyImpaired</span></span>  |
| <span data-ttu-id="90339-120">3</span><span class="sxs-lookup"><span data-stu-id="90339-120">3</span></span>     | <span data-ttu-id="90339-121">DirectorComments1</span><span class="sxs-lookup"><span data-stu-id="90339-121">DirectorComments1</span></span> |
| <span data-ttu-id="90339-122">4</span><span class="sxs-lookup"><span data-stu-id="90339-122">4</span></span>     | <span data-ttu-id="90339-123">DirectorComments2</span><span class="sxs-lookup"><span data-stu-id="90339-123">DirectorComments2</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90339-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="90339-124">Return Value</span></span>

<span data-ttu-id="90339-125">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="90339-125">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="90339-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90339-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90339-127">MSWebDVD 物件</span><span class="sxs-lookup"><span data-stu-id="90339-127">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



