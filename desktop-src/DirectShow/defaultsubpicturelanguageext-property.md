---
description: DefaultSubpictureLanguageExt 屬性會抓取預設的 DVD 子圖片語言延伸模組。
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: DefaultSubpictureLanguageExt 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509848"
---
# <a name="defaultsubpicturelanguageext-property"></a><span data-ttu-id="14ebf-103">DefaultSubpictureLanguageExt 屬性</span><span class="sxs-lookup"><span data-stu-id="14ebf-103">DefaultSubpictureLanguageExt Property</span></span>

> [!Note]  
> <span data-ttu-id="14ebf-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="14ebf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="14ebf-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="14ebf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="14ebf-106">屬性會抓取 `DefaultSubpictureLanguageExt` 預設的 DVD 子圖片語言延伸模組。</span><span class="sxs-lookup"><span data-stu-id="14ebf-106">The `DefaultSubpictureLanguageExt` property retrieves the default DVD subpicture language extension.</span></span>

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a><span data-ttu-id="14ebf-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="14ebf-107">Return Value</span></span>

<span data-ttu-id="14ebf-108">傳回整數值，指出預設的 DVD 子圖片語言延伸模組。</span><span class="sxs-lookup"><span data-stu-id="14ebf-108">Returns an Integer value indicating the default DVD subpicture language extension.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ebf-109">備註</span><span class="sxs-lookup"><span data-stu-id="14ebf-109">Remarks</span></span>

<span data-ttu-id="14ebf-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="14ebf-110">This property is read-only with no default value.</span></span> <span data-ttu-id="14ebf-111">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="14ebf-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="14ebf-112">值</span><span class="sxs-lookup"><span data-stu-id="14ebf-112">Value</span></span> | <span data-ttu-id="14ebf-113">描述</span><span class="sxs-lookup"><span data-stu-id="14ebf-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="14ebf-114">0</span><span class="sxs-lookup"><span data-stu-id="14ebf-114">0</span></span>     | <span data-ttu-id="14ebf-115">未指定擴充功能</span><span class="sxs-lookup"><span data-stu-id="14ebf-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="14ebf-116">1</span><span class="sxs-lookup"><span data-stu-id="14ebf-116">1</span></span>     | <span data-ttu-id="14ebf-117">一般字幕</span><span class="sxs-lookup"><span data-stu-id="14ebf-117">Normal Captions</span></span>                |
| <span data-ttu-id="14ebf-118">2</span><span class="sxs-lookup"><span data-stu-id="14ebf-118">2</span></span>     | <span data-ttu-id="14ebf-119">大標題</span><span class="sxs-lookup"><span data-stu-id="14ebf-119">Big Captions</span></span>                   |
| <span data-ttu-id="14ebf-120">3</span><span class="sxs-lookup"><span data-stu-id="14ebf-120">3</span></span>     | <span data-ttu-id="14ebf-121">子女的標題</span><span class="sxs-lookup"><span data-stu-id="14ebf-121">Children's Captions</span></span>            |
| <span data-ttu-id="14ebf-122">5</span><span class="sxs-lookup"><span data-stu-id="14ebf-122">5</span></span>     | <span data-ttu-id="14ebf-123">一般隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="14ebf-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="14ebf-124">6</span><span class="sxs-lookup"><span data-stu-id="14ebf-124">6</span></span>     | <span data-ttu-id="14ebf-125">大型隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="14ebf-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="14ebf-126">7</span><span class="sxs-lookup"><span data-stu-id="14ebf-126">7</span></span>     | <span data-ttu-id="14ebf-127">兒童隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="14ebf-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="14ebf-128">9</span><span class="sxs-lookup"><span data-stu-id="14ebf-128">9</span></span>     | <span data-ttu-id="14ebf-129">Forced</span><span class="sxs-lookup"><span data-stu-id="14ebf-129">Forced</span></span>                         |
| <span data-ttu-id="14ebf-130">13</span><span class="sxs-lookup"><span data-stu-id="14ebf-130">13</span></span>    | <span data-ttu-id="14ebf-131">一般導演的留言</span><span class="sxs-lookup"><span data-stu-id="14ebf-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="14ebf-132">14</span><span class="sxs-lookup"><span data-stu-id="14ebf-132">14</span></span>    | <span data-ttu-id="14ebf-133">大型總監的評論</span><span class="sxs-lookup"><span data-stu-id="14ebf-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="14ebf-134">15</span><span class="sxs-lookup"><span data-stu-id="14ebf-134">15</span></span>    | <span data-ttu-id="14ebf-135">子女的 Director's 批註</span><span class="sxs-lookup"><span data-stu-id="14ebf-135">Children's Director's Comments</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="14ebf-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14ebf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ebf-137">**SelectDefaultSubpictureLanguage**</span><span class="sxs-lookup"><span data-stu-id="14ebf-137">**SelectDefaultSubpictureLanguage**</span></span>](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



