---
title: CounterItem. ScaleFactor 屬性
description: 抓取或設定用來繪製計數器值的比例因數。
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- ScaleFactor 屬性 SysMon
- ScaleFactor 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，ScaleFactor 屬性
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965498"
---
# <a name="counteritemscalefactor-property"></a><span data-ttu-id="6079e-106">CounterItem. ScaleFactor 屬性</span><span class="sxs-lookup"><span data-stu-id="6079e-106">CounterItem.ScaleFactor property</span></span>

<span data-ttu-id="6079e-107">抓取或設定用來繪製計數器值的比例因數。</span><span class="sxs-lookup"><span data-stu-id="6079e-107">Retrieves or sets the scale factor used to graph the counter value.</span></span>

<span data-ttu-id="6079e-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6079e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6079e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6079e-109">Syntax</span></span>


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a><span data-ttu-id="6079e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6079e-110">Property value</span></span>

<span data-ttu-id="6079e-111">用來顯示圖形化計數器值的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="6079e-111">Scale factor used in displaying the graphed counter values.</span></span> <span data-ttu-id="6079e-112">有效值的範圍為-9 到 9 (值會對應至 0.000000001-100000000.0) 。</span><span class="sxs-lookup"><span data-stu-id="6079e-112">Valid values range from -9 to 9 (the values correspond to 0.000000001 - 100000000.0).</span></span>

<span data-ttu-id="6079e-113">**在 Windows Vista 之前：** 有效值的範圍為-7 到 7 (值對應至 0.0000001-1000000.0) 。</span><span class="sxs-lookup"><span data-stu-id="6079e-113">**Prior to Windows Vista:** Valid values range from -7 to 7 (the values correspond to 0.0000001 - 1000000.0).</span></span>

## <a name="remarks"></a><span data-ttu-id="6079e-114">備註</span><span class="sxs-lookup"><span data-stu-id="6079e-114">Remarks</span></span>

<span data-ttu-id="6079e-115">只有當您想要變更計數器的預設縮放比例時，才設定此屬性 (每個計數器都會定義自己的比例因數) 。</span><span class="sxs-lookup"><span data-stu-id="6079e-115">Only set this property if you want to change the counter's default scale factor (each counter defines its own scale factor).</span></span> <span data-ttu-id="6079e-116">如果計數器使用其預設比例因數來繪製值，則這個屬性的值會設定為正整數。</span><span class="sxs-lookup"><span data-stu-id="6079e-116">The value of this property is set to Integer.MaxValue if the counter is using its default scale factor to graph the values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6079e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6079e-117">Requirements</span></span>



| <span data-ttu-id="6079e-118">需求</span><span class="sxs-lookup"><span data-stu-id="6079e-118">Requirement</span></span> | <span data-ttu-id="6079e-119">值</span><span class="sxs-lookup"><span data-stu-id="6079e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6079e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6079e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6079e-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6079e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6079e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6079e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6079e-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6079e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6079e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6079e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6079e-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6079e-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6079e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6079e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6079e-127">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="6079e-127">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="6079e-128">**SystemMonitor.ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="6079e-128">**SystemMonitor.ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





