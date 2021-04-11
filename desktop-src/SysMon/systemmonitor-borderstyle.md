---
title: SystemMonitor 屬性
description: 抓取或設定控制項的框線樣式。
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- BorderStyle 屬性 SysMon
- BorderStyle 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，BorderStyle 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843472"
---
# <a name="systemmonitorborderstyle-property"></a><span data-ttu-id="846b6-106">SystemMonitor 屬性</span><span class="sxs-lookup"><span data-stu-id="846b6-106">SystemMonitor.BorderStyle property</span></span>

<span data-ttu-id="846b6-107">抓取或設定控制項的框線樣式。</span><span class="sxs-lookup"><span data-stu-id="846b6-107">Retrieves or sets the border style of the control.</span></span>

<span data-ttu-id="846b6-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="846b6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="846b6-109">語法</span><span class="sxs-lookup"><span data-stu-id="846b6-109">Syntax</span></span>


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="846b6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="846b6-110">Property value</span></span>

<span data-ttu-id="846b6-111">控制項的框線樣式。</span><span class="sxs-lookup"><span data-stu-id="846b6-111">Border style of the control.</span></span>

<span data-ttu-id="846b6-112">您可以將此屬性設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="846b6-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="846b6-113">值</span><span class="sxs-lookup"><span data-stu-id="846b6-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="846b6-114">意義</span><span class="sxs-lookup"><span data-stu-id="846b6-114">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <span data-ttu-id="846b6-115"><dt>**FormBorderStyle. VbBSNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="846b6-115"><dt>**System.Windows.Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="846b6-116">無框線。</span><span class="sxs-lookup"><span data-stu-id="846b6-116">No border.</span></span> <span data-ttu-id="846b6-117">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="846b6-117">This is the default value.</span></span><br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <span data-ttu-id="846b6-118"><dt>**FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="846b6-118"><dt>**System.Windows.Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="846b6-119">固定、單一框線。</span><span class="sxs-lookup"><span data-stu-id="846b6-119">Fixed, single border.</span></span><br/>                 |



 

## <a name="exceptions"></a><span data-ttu-id="846b6-120">例外狀況</span><span class="sxs-lookup"><span data-stu-id="846b6-120">Exceptions</span></span>



| <span data-ttu-id="846b6-121">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="846b6-121">Exception type</span></span>               | <span data-ttu-id="846b6-122">條件</span><span class="sxs-lookup"><span data-stu-id="846b6-122">Condition</span></span>                                |
|------------------------------|------------------------------------------|
| <span data-ttu-id="846b6-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="846b6-123">**System.ArgumentException**</span></span> | <span data-ttu-id="846b6-124">指定的框線樣式無效。</span><span class="sxs-lookup"><span data-stu-id="846b6-124">The specified border style is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="846b6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="846b6-125">Requirements</span></span>



| <span data-ttu-id="846b6-126">需求</span><span class="sxs-lookup"><span data-stu-id="846b6-126">Requirement</span></span> | <span data-ttu-id="846b6-127">值</span><span class="sxs-lookup"><span data-stu-id="846b6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="846b6-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="846b6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="846b6-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="846b6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="846b6-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="846b6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="846b6-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="846b6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="846b6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="846b6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="846b6-133"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="846b6-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="846b6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="846b6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="846b6-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="846b6-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





