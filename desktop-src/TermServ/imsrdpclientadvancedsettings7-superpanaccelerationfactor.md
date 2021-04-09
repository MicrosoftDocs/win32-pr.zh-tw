---
title: IMsRdpClientAdvancedSettings7 SuperPanAccelerationFactor 屬性
description: 指定或抓取表示 SuperPan 加速因素的值。 SuperPan 加速因素決定在 SuperPan 模式下，螢幕的移動速度。
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- SuperPanAccelerationFactor 屬性遠端桌面服務
- SuperPanAccelerationFactor 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，SuperPanAccelerationFactor 屬性
- SuperPanAccelerationFactor 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，SuperPanAccelerationFactor 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935135"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a><span data-ttu-id="f93f8-109">IMsRdpClientAdvancedSettings7：： SuperPanAccelerationFactor 屬性</span><span class="sxs-lookup"><span data-stu-id="f93f8-109">IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor property</span></span>

<span data-ttu-id="f93f8-110">指定或抓取表示 SuperPan 加速因素的值。</span><span class="sxs-lookup"><span data-stu-id="f93f8-110">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span> <span data-ttu-id="f93f8-111">SuperPan 加速因素決定在 SuperPan 模式下，螢幕的移動速度。</span><span class="sxs-lookup"><span data-stu-id="f93f8-111">The SuperPan acceleration factor determines how quickly the screen pans when in SuperPan mode.</span></span> <span data-ttu-id="f93f8-112">加速因數是在用戶端的每個滑鼠移動圖元的指定方向，螢幕視圖所滾動的圖元數。</span><span class="sxs-lookup"><span data-stu-id="f93f8-112">The acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement by the client.</span></span>

<span data-ttu-id="f93f8-113">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f93f8-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f93f8-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="f93f8-114">Syntax</span></span>


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a><span data-ttu-id="f93f8-115">屬性值</span><span class="sxs-lookup"><span data-stu-id="f93f8-115">Property value</span></span>

<span data-ttu-id="f93f8-116">要設定的 SuperPan 加速因素。</span><span class="sxs-lookup"><span data-stu-id="f93f8-116">The SuperPan acceleration factor to set.</span></span> <span data-ttu-id="f93f8-117">SuperPan 加速因素是螢幕視圖在每個滑鼠移動圖元的指定方向滾動的圖元數。</span><span class="sxs-lookup"><span data-stu-id="f93f8-117">The SuperPan acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement.</span></span>

## <a name="remarks"></a><span data-ttu-id="f93f8-118">備註</span><span class="sxs-lookup"><span data-stu-id="f93f8-118">Remarks</span></span>

<span data-ttu-id="f93f8-119">如需 SuperPan 的詳細資訊，請參閱 [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)。</span><span class="sxs-lookup"><span data-stu-id="f93f8-119">For more information about SuperPan, see [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f93f8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f93f8-120">Requirements</span></span>



| <span data-ttu-id="f93f8-121">需求</span><span class="sxs-lookup"><span data-stu-id="f93f8-121">Requirement</span></span> | <span data-ttu-id="f93f8-122">值</span><span class="sxs-lookup"><span data-stu-id="f93f8-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f93f8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f93f8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f93f8-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f93f8-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="f93f8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f93f8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f93f8-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f93f8-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="f93f8-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f93f8-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="f93f8-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f93f8-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f93f8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f93f8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f93f8-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f93f8-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f93f8-131">IID</span><span class="sxs-lookup"><span data-stu-id="f93f8-131">IID</span></span><br/>                      | <span data-ttu-id="f93f8-132">IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="f93f8-132">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f93f8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f93f8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f93f8-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f93f8-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f93f8-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f93f8-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f93f8-136">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="f93f8-136">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





