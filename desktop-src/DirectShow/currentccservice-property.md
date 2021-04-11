---
description: CurrentCCService 屬性會設定或抓取目前的隱藏式輔助字幕服務。
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: CurrentCCService 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846476"
---
# <a name="currentccservice-property"></a><span data-ttu-id="203a7-103">CurrentCCService 屬性</span><span class="sxs-lookup"><span data-stu-id="203a7-103">CurrentCCService Property</span></span>

> [!Note]  
> <span data-ttu-id="203a7-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="203a7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="203a7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="203a7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="203a7-106">`CurrentCCService`屬性會設定或抓取目前的隱藏式輔助字幕服務。</span><span class="sxs-lookup"><span data-stu-id="203a7-106">The `CurrentCCService` property sets or retrieves the current closed captioning service.</span></span>

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a><span data-ttu-id="203a7-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="203a7-107">Return Value</span></span>

<span data-ttu-id="203a7-108">傳回整數值，表示已啟用隱藏式輔助字幕服務的類型。</span><span class="sxs-lookup"><span data-stu-id="203a7-108">Returns an integer value indicating the type of closed captioning service enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="203a7-109">備註</span><span class="sxs-lookup"><span data-stu-id="203a7-109">Remarks</span></span>

<span data-ttu-id="203a7-110">這個屬性的可能值為：</span><span class="sxs-lookup"><span data-stu-id="203a7-110">The possible values of this property are:</span></span>



| <span data-ttu-id="203a7-111">值</span><span class="sxs-lookup"><span data-stu-id="203a7-111">Value</span></span> | <span data-ttu-id="203a7-112">描述</span><span class="sxs-lookup"><span data-stu-id="203a7-112">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="203a7-113">0x0</span><span class="sxs-lookup"><span data-stu-id="203a7-113">0x0</span></span>   | <span data-ttu-id="203a7-114">沒有目前的服務。</span><span class="sxs-lookup"><span data-stu-id="203a7-114">No current service.</span></span> <span data-ttu-id="203a7-115">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="203a7-115">This is the default value.</span></span>                       |
| <span data-ttu-id="203a7-116">0x1</span><span class="sxs-lookup"><span data-stu-id="203a7-116">0x1</span></span>   | <span data-ttu-id="203a7-117">真正的標題，第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="203a7-117">True captioning, first field.</span></span> <span data-ttu-id="203a7-118">預設服務。</span><span class="sxs-lookup"><span data-stu-id="203a7-118">Default service.</span></span>                       |
| <span data-ttu-id="203a7-119">0x2</span><span class="sxs-lookup"><span data-stu-id="203a7-119">0x2</span></span>   | <span data-ttu-id="203a7-120">次要語言的標題，第二個欄位。</span><span class="sxs-lookup"><span data-stu-id="203a7-120">Captioning for secondary language, second field.</span></span> <span data-ttu-id="203a7-121">通常不會使用。</span><span class="sxs-lookup"><span data-stu-id="203a7-121">Generally not used.</span></span> |



 

<span data-ttu-id="203a7-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="203a7-122">This property is read/write.</span></span>

## <a name="see-also"></a><span data-ttu-id="203a7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="203a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203a7-124">**CCActive**</span><span class="sxs-lookup"><span data-stu-id="203a7-124">**CCActive**</span></span>](ccactive-property.md)
</dt> </dl>

 

 



