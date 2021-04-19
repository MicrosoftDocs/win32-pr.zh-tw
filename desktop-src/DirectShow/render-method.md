---
description: Render 方法會初始化 DVD 篩選圖形。
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Render 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991593"
---
# <a name="render-method"></a><span data-ttu-id="d3329-103">Render 方法</span><span class="sxs-lookup"><span data-stu-id="d3329-103">Render Method</span></span>

> [!Note]  
> <span data-ttu-id="d3329-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="d3329-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d3329-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d3329-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d3329-106">`Render`方法會初始化 DVD 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="d3329-106">The `Render` method initializes the DVD filter graph.</span></span>

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a><span data-ttu-id="d3329-107">參數</span><span class="sxs-lookup"><span data-stu-id="d3329-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3329-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span><span class="sxs-lookup"><span data-stu-id="d3329-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span></span>
</dt> <dd>

<span data-ttu-id="d3329-109">指定整數值，指出是否將終結和重建篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="d3329-109">Specifies an integer value indicating whether the filter graph will be destroyed and rebuilt.</span></span>



| <span data-ttu-id="d3329-110">值</span><span class="sxs-lookup"><span data-stu-id="d3329-110">Value</span></span> | <span data-ttu-id="d3329-111">描述</span><span class="sxs-lookup"><span data-stu-id="d3329-111">Description</span></span>                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3329-112">0</span><span class="sxs-lookup"><span data-stu-id="d3329-112">0</span></span>     | <span data-ttu-id="d3329-113">如果篩選圖形已經存在，將不會終結並重建。</span><span class="sxs-lookup"><span data-stu-id="d3329-113">The filter graph will not be destroyed and rebuilt if it already exists.</span></span> <span data-ttu-id="d3329-114">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="d3329-114">This is the default value.</span></span> |
| <span data-ttu-id="d3329-115">1</span><span class="sxs-lookup"><span data-stu-id="d3329-115">1</span></span>     | <span data-ttu-id="d3329-116">篩選圖形將會損毀並重建（如果已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="d3329-116">The filter graph will be destroyed and rebuilt if it already exists.</span></span>                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3329-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3329-117">Return Value</span></span>

<span data-ttu-id="d3329-118">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="d3329-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3329-119">備註</span><span class="sxs-lookup"><span data-stu-id="d3329-119">Remarks</span></span>

<span data-ttu-id="d3329-120">`Render`方法可讓 **MSWebDVD** 物件在啟動時完全初始化基礎 DirectShow 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="d3329-120">The `Render` method enables the **MSWebDVD** object to fully initialize the underlying DirectShow filter graph on startup.</span></span> <span data-ttu-id="d3329-121">這可避免使用者發出第一個命令來播放光碟或顯示功能表時，所發生的輕微延遲。</span><span class="sxs-lookup"><span data-stu-id="d3329-121">This eliminates the slight delay that otherwise occurs when the user issues the first command to play a disc or show a menu.</span></span> <span data-ttu-id="d3329-122">在 `Render` 呼叫任何其他方法之前，不需要呼叫任何情況。</span><span class="sxs-lookup"><span data-stu-id="d3329-122">There is no case in which `Render` needs to be called before calling any other method.</span></span> <span data-ttu-id="d3329-123">例如，如果應用程式在初始化篩選圖形之前呼叫 [**PlayTitle**](playtitle-method.md) ， **MSWebDVD** 物件 `Render` 就會自動呼叫，然後再嘗試播放光碟。</span><span class="sxs-lookup"><span data-stu-id="d3329-123">For example, if the application calls [**PlayTitle**](playtitle-method.md) before the filter graph has been initialized, the **MSWebDVD** object calls `Render` automatically before attempting to play the disc.</span></span>

 

 



