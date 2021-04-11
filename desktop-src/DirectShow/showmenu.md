---
description: 當光碟啟用或停用功能表的顯示時，就會傳送 ShowMenu 事件。
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935869"
---
# <a name="showmenu"></a><span data-ttu-id="d9e52-103">ShowMenu</span><span class="sxs-lookup"><span data-stu-id="d9e52-103">ShowMenu</span></span>

> [!Note]  
> <span data-ttu-id="d9e52-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="d9e52-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d9e52-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d9e52-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d9e52-106">`ShowMenu`當光碟啟用或停用功能表的顯示時，就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="d9e52-106">The `ShowMenu` event is sent when the disc enables or disables the showing of a menu.</span></span>

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a><span data-ttu-id="d9e52-107">參數</span><span class="sxs-lookup"><span data-stu-id="d9e52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e52-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span><span class="sxs-lookup"><span data-stu-id="d9e52-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span></span>
</dt> <dd>

<span data-ttu-id="d9e52-109">指定哪些功能表已啟用或停用為數字值。</span><span class="sxs-lookup"><span data-stu-id="d9e52-109">Specifies which menu has been enabled or disabled as a Number value.</span></span>



| <span data-ttu-id="d9e52-110">值</span><span class="sxs-lookup"><span data-stu-id="d9e52-110">Value</span></span> | <span data-ttu-id="d9e52-111">描述</span><span class="sxs-lookup"><span data-stu-id="d9e52-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="d9e52-112">2</span><span class="sxs-lookup"><span data-stu-id="d9e52-112">2</span></span>     | <span data-ttu-id="d9e52-113">標題</span><span class="sxs-lookup"><span data-stu-id="d9e52-113">Title</span></span>       |
| <span data-ttu-id="d9e52-114">3</span><span class="sxs-lookup"><span data-stu-id="d9e52-114">3</span></span>     | <span data-ttu-id="d9e52-115">Root</span><span class="sxs-lookup"><span data-stu-id="d9e52-115">Root</span></span>        |
| <span data-ttu-id="d9e52-116">4</span><span class="sxs-lookup"><span data-stu-id="d9e52-116">4</span></span>     | <span data-ttu-id="d9e52-117">子圖片</span><span class="sxs-lookup"><span data-stu-id="d9e52-117">Subpicture</span></span>  |
| <span data-ttu-id="d9e52-118">5</span><span class="sxs-lookup"><span data-stu-id="d9e52-118">5</span></span>     | <span data-ttu-id="d9e52-119">音訊</span><span class="sxs-lookup"><span data-stu-id="d9e52-119">Audio</span></span>       |
| <span data-ttu-id="d9e52-120">6</span><span class="sxs-lookup"><span data-stu-id="d9e52-120">6</span></span>     | <span data-ttu-id="d9e52-121">角度</span><span class="sxs-lookup"><span data-stu-id="d9e52-121">Angle</span></span>       |
| <span data-ttu-id="d9e52-122">7</span><span class="sxs-lookup"><span data-stu-id="d9e52-122">7</span></span>     | <span data-ttu-id="d9e52-123">章節</span><span class="sxs-lookup"><span data-stu-id="d9e52-123">Chapter</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d9e52-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="d9e52-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="d9e52-125">指定作業是否啟用或停用為布林值。</span><span class="sxs-lookup"><span data-stu-id="d9e52-125">Specifies whether the operation is enabled or disabled as a Boolean.</span></span>

</dd> </dl>

 

 



