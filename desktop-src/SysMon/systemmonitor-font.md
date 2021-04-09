---
title: SystemMonitor 字型屬性
description: 抓取或設定控制項中所使用的字型。
ms.assetid: 973ac31e-33e6-4280-ba0b-5b9f5f7563e7
keywords:
- 字型屬性 SysMon
- Font 屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，字型屬性
topic_type:
- apiref
api_name:
- SystemMonitor.Font
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2abf021000d673474bb006d9d16afa459ddbdb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685941"
---
# <a name="systemmonitorfont-property"></a><span data-ttu-id="e7473-106">SystemMonitor 字型屬性</span><span class="sxs-lookup"><span data-stu-id="e7473-106">SystemMonitor.Font property</span></span>

<span data-ttu-id="e7473-107">抓取或設定控制項中所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="e7473-107">Retrieves or sets the font used in the control.</span></span>

<span data-ttu-id="e7473-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e7473-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7473-109">語法</span><span class="sxs-lookup"><span data-stu-id="e7473-109">Syntax</span></span>


```VB
Property Font As stdole.IFontDisp
```



## <a name="property-value"></a><span data-ttu-id="e7473-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e7473-110">Property value</span></span>

<span data-ttu-id="e7473-111">用來在控制項中顯示文字的字型。</span><span class="sxs-lookup"><span data-stu-id="e7473-111">Font used to display text in the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7473-112">備註</span><span class="sxs-lookup"><span data-stu-id="e7473-112">Remarks</span></span>

<span data-ttu-id="e7473-113">這是環境屬性。</span><span class="sxs-lookup"><span data-stu-id="e7473-113">This is an ambient property.</span></span> <span data-ttu-id="e7473-114">這個屬性的值是由容器所決定。</span><span class="sxs-lookup"><span data-stu-id="e7473-114">The value of this property is determined by the container.</span></span> <span data-ttu-id="e7473-115">設定這個屬性的值可能會影響控制項和容器的假像成為單一應用程式。</span><span class="sxs-lookup"><span data-stu-id="e7473-115">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7473-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7473-116">Requirements</span></span>



| <span data-ttu-id="e7473-117">需求</span><span class="sxs-lookup"><span data-stu-id="e7473-117">Requirement</span></span> | <span data-ttu-id="e7473-118">值</span><span class="sxs-lookup"><span data-stu-id="e7473-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7473-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7473-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7473-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7473-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e7473-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7473-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7473-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7473-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7473-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e7473-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7473-124"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e7473-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7473-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7473-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7473-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e7473-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="e7473-127">**SystemMonitor 的前景**</span><span class="sxs-lookup"><span data-stu-id="e7473-127">**SystemMonitor.ForeColor**</span></span>](systemmonitor-forecolor.md)
</dt> </dl>

 

 





