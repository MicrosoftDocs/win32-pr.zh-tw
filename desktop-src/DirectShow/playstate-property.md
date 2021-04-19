---
description: PlayState 屬性會捕獲 MSWebDVD 物件的目前狀態。
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: PlayState 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106990918"
---
# <a name="playstate-property"></a><span data-ttu-id="65b99-103">PlayState 屬性</span><span class="sxs-lookup"><span data-stu-id="65b99-103">PlayState Property</span></span>

> [!Note]  
> <span data-ttu-id="65b99-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="65b99-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="65b99-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="65b99-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="65b99-106">`PlayState`屬性會捕獲 **MSWebDVD** 物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="65b99-106">The `PlayState` property retrieves the current state of the **MSWebDVD** object.</span></span>

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a><span data-ttu-id="65b99-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="65b99-107">Return Value</span></span>

<span data-ttu-id="65b99-108">傳回整數值，代表 DVD 導覽器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="65b99-108">Returns an Integer value representing the current state of the DVD Navigator.</span></span>



| <span data-ttu-id="65b99-109">傳回碼</span><span class="sxs-lookup"><span data-stu-id="65b99-109">Return code</span></span> | <span data-ttu-id="65b99-110">Description</span><span class="sxs-lookup"><span data-stu-id="65b99-110">Description</span></span>   |
|-------------|---------------|
| <span data-ttu-id="65b99-111">-2</span><span class="sxs-lookup"><span data-stu-id="65b99-111">-2</span></span>          | <span data-ttu-id="65b99-112">未定義</span><span class="sxs-lookup"><span data-stu-id="65b99-112">Undefined</span></span>     |
| <span data-ttu-id="65b99-113">-1</span><span class="sxs-lookup"><span data-stu-id="65b99-113">-1</span></span>          | <span data-ttu-id="65b99-114">未初始化：</span><span class="sxs-lookup"><span data-stu-id="65b99-114">Uninitialized</span></span> |
| <span data-ttu-id="65b99-115">0</span><span class="sxs-lookup"><span data-stu-id="65b99-115">0</span></span>           | <span data-ttu-id="65b99-116">已停止</span><span class="sxs-lookup"><span data-stu-id="65b99-116">Stopped</span></span>       |
| <span data-ttu-id="65b99-117">1</span><span class="sxs-lookup"><span data-stu-id="65b99-117">1</span></span>           | <span data-ttu-id="65b99-118">已暫停</span><span class="sxs-lookup"><span data-stu-id="65b99-118">Paused</span></span>        |
| <span data-ttu-id="65b99-119">2</span><span class="sxs-lookup"><span data-stu-id="65b99-119">2</span></span>           | <span data-ttu-id="65b99-120">執行中</span><span class="sxs-lookup"><span data-stu-id="65b99-120">Running</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="65b99-121">備註</span><span class="sxs-lookup"><span data-stu-id="65b99-121">Remarks</span></span>

<span data-ttu-id="65b99-122">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="65b99-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="65b99-123">**MSWebDVD** 物件可控制 [DirectShow dvd 瀏覽器] 篩選器，其會執行 DVD 流覽的實際工作。</span><span class="sxs-lookup"><span data-stu-id="65b99-123">The **MSWebDVD** object controls the DirectShow DVD Navigator filter, which does the actual work of DVD navigation.</span></span> <span data-ttu-id="65b99-124">這實際上是此屬性所參考 DVD 導覽器的狀態。</span><span class="sxs-lookup"><span data-stu-id="65b99-124">It is actually the state of the DVD Navigator that this property refers to.</span></span> <span data-ttu-id="65b99-125">DVD 導覽器可以是數種狀態的其中一種，如上面所述。</span><span class="sxs-lookup"><span data-stu-id="65b99-125">The DVD Navigator can be in one of several states, as described above.</span></span> <span data-ttu-id="65b99-126">`PlayState`屬性可以用來做為診斷工具，但通常不會有任何原因讓腳本應用程式監視 DVD 導覽器的狀態。</span><span class="sxs-lookup"><span data-stu-id="65b99-126">The `PlayState` property can be useful as a diagnostic tool, but generally there should be no reason for a scripting application to monitor the state of the DVD Navigator.</span></span>

 

 



