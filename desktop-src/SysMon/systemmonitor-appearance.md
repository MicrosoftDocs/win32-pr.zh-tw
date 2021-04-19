---
title: SystemMonitor 外觀屬性
description: 抓取或設定控制項的外觀，以包含或省略三維顯示效果。
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- 外觀屬性 SysMon
- 外觀屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，外觀屬性
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991302"
---
# <a name="systemmonitorappearance-property"></a><span data-ttu-id="6aad4-106">SystemMonitor 外觀屬性</span><span class="sxs-lookup"><span data-stu-id="6aad4-106">SystemMonitor.Appearance property</span></span>

<span data-ttu-id="6aad4-107">抓取或設定控制項的外觀，以包含或省略三維顯示效果。</span><span class="sxs-lookup"><span data-stu-id="6aad4-107">Retrieves or sets the control's appearance to include or omit three-dimensional display effects.</span></span>

<span data-ttu-id="6aad4-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6aad4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aad4-109">語法</span><span class="sxs-lookup"><span data-stu-id="6aad4-109">Syntax</span></span>


```VB
Property Appearance As Long
```



## <a name="property-value"></a><span data-ttu-id="6aad4-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6aad4-110">Property value</span></span>

<span data-ttu-id="6aad4-111">外觀值，決定是否以立體效果繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="6aad4-111">Appearance value that determines if the control is painted with three-dimensional effects.</span></span>

<span data-ttu-id="6aad4-112">您可以將此屬性設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6aad4-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="6aad4-113">值</span><span class="sxs-lookup"><span data-stu-id="6aad4-113">Value</span></span>                                                                        | <span data-ttu-id="6aad4-114">意義</span><span class="sxs-lookup"><span data-stu-id="6aad4-114">Meaning</span></span>                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6aad4-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6aad4-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6aad4-116">繪製沒有視覺效果的控制項。</span><span class="sxs-lookup"><span data-stu-id="6aad4-116">Paints the control without visual effects.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6aad4-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6aad4-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6aad4-118">繪製具有立體效果的控制項。</span><span class="sxs-lookup"><span data-stu-id="6aad4-118">Paints the control with three-dimensional effects.</span></span> <span data-ttu-id="6aad4-119">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="6aad4-119">This is the default value.</span></span><br/> |



 

## <a name="exceptions"></a><span data-ttu-id="6aad4-120">例外狀況</span><span class="sxs-lookup"><span data-stu-id="6aad4-120">Exceptions</span></span>



| <span data-ttu-id="6aad4-121">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="6aad4-121">Exception type</span></span>               | <span data-ttu-id="6aad4-122">條件</span><span class="sxs-lookup"><span data-stu-id="6aad4-122">Condition</span></span>                                    |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="6aad4-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="6aad4-123">**System.ArgumentException**</span></span> | <span data-ttu-id="6aad4-124">指定的外觀值無效。</span><span class="sxs-lookup"><span data-stu-id="6aad4-124">The specified appearance value is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6aad4-125">備註</span><span class="sxs-lookup"><span data-stu-id="6aad4-125">Remarks</span></span>

<span data-ttu-id="6aad4-126">這是環境屬性。</span><span class="sxs-lookup"><span data-stu-id="6aad4-126">This is an ambient property.</span></span> <span data-ttu-id="6aad4-127">這個屬性的值是由容器所決定。</span><span class="sxs-lookup"><span data-stu-id="6aad4-127">The value of this property is determined by the container.</span></span> <span data-ttu-id="6aad4-128">設定這個屬性的值可能會影響控制項和容器的假像成為單一應用程式。</span><span class="sxs-lookup"><span data-stu-id="6aad4-128">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aad4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6aad4-129">Requirements</span></span>



| <span data-ttu-id="6aad4-130">需求</span><span class="sxs-lookup"><span data-stu-id="6aad4-130">Requirement</span></span> | <span data-ttu-id="6aad4-131">值</span><span class="sxs-lookup"><span data-stu-id="6aad4-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6aad4-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6aad4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6aad4-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6aad4-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6aad4-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6aad4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6aad4-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6aad4-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6aad4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6aad4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aad4-137"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6aad4-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aad4-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6aad4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aad4-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="6aad4-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





