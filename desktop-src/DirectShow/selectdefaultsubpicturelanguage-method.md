---
description: SelectDefaultSubpictureLanguage 方法會在 MSWebDVD 物件中設定目前的預設子圖片語言。
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: SelectDefaultSubpictureLanguage 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687800"
---
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="3b582-103">SelectDefaultSubpictureLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="3b582-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="3b582-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="3b582-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3b582-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="3b582-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3b582-106">`SelectDefaultSubpictureLanguage`方法會在 **MSWebDVD** 物件中設定目前的預設子圖片語言。</span><span class="sxs-lookup"><span data-stu-id="3b582-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="3b582-107">參數</span><span class="sxs-lookup"><span data-stu-id="3b582-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b582-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="3b582-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="3b582-109">將語言指定為整數。</span><span class="sxs-lookup"><span data-stu-id="3b582-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="3b582-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="3b582-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="3b582-111">將子圖片語言延伸模組指定為整數。</span><span class="sxs-lookup"><span data-stu-id="3b582-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="3b582-112">值</span><span class="sxs-lookup"><span data-stu-id="3b582-112">Value</span></span> | <span data-ttu-id="3b582-113">描述</span><span class="sxs-lookup"><span data-stu-id="3b582-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="3b582-114">0</span><span class="sxs-lookup"><span data-stu-id="3b582-114">0</span></span>     | <span data-ttu-id="3b582-115">未指定擴充功能</span><span class="sxs-lookup"><span data-stu-id="3b582-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="3b582-116">1</span><span class="sxs-lookup"><span data-stu-id="3b582-116">1</span></span>     | <span data-ttu-id="3b582-117">一般字幕</span><span class="sxs-lookup"><span data-stu-id="3b582-117">Normal Captions</span></span>                |
| <span data-ttu-id="3b582-118">2</span><span class="sxs-lookup"><span data-stu-id="3b582-118">2</span></span>     | <span data-ttu-id="3b582-119">大標題</span><span class="sxs-lookup"><span data-stu-id="3b582-119">Big Captions</span></span>                   |
| <span data-ttu-id="3b582-120">3</span><span class="sxs-lookup"><span data-stu-id="3b582-120">3</span></span>     | <span data-ttu-id="3b582-121">子女的標題</span><span class="sxs-lookup"><span data-stu-id="3b582-121">Children's Captions</span></span>            |
| <span data-ttu-id="3b582-122">5</span><span class="sxs-lookup"><span data-stu-id="3b582-122">5</span></span>     | <span data-ttu-id="3b582-123">一般隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="3b582-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="3b582-124">6</span><span class="sxs-lookup"><span data-stu-id="3b582-124">6</span></span>     | <span data-ttu-id="3b582-125">大型隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="3b582-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="3b582-126">7</span><span class="sxs-lookup"><span data-stu-id="3b582-126">7</span></span>     | <span data-ttu-id="3b582-127">兒童隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="3b582-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="3b582-128">9</span><span class="sxs-lookup"><span data-stu-id="3b582-128">9</span></span>     | <span data-ttu-id="3b582-129">Forced</span><span class="sxs-lookup"><span data-stu-id="3b582-129">Forced</span></span>                         |
| <span data-ttu-id="3b582-130">13</span><span class="sxs-lookup"><span data-stu-id="3b582-130">13</span></span>    | <span data-ttu-id="3b582-131">一般導演的留言</span><span class="sxs-lookup"><span data-stu-id="3b582-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="3b582-132">14</span><span class="sxs-lookup"><span data-stu-id="3b582-132">14</span></span>    | <span data-ttu-id="3b582-133">大型總監的評論</span><span class="sxs-lookup"><span data-stu-id="3b582-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="3b582-134">15</span><span class="sxs-lookup"><span data-stu-id="3b582-134">15</span></span>    | <span data-ttu-id="3b582-135">子女的 Director's 批註</span><span class="sxs-lookup"><span data-stu-id="3b582-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b582-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b582-136">Return Value</span></span>

<span data-ttu-id="3b582-137">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="3b582-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b582-138">備註</span><span class="sxs-lookup"><span data-stu-id="3b582-138">Remarks</span></span>

<span data-ttu-id="3b582-139">子圖片語言延伸模組提供有關子圖片的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="3b582-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



