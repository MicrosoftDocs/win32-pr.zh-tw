---
title: IMsRdpClientAdvancedSettings6 RelativeMouseMode 屬性
description: 指定滑鼠是否應使用相對模式。
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- RelativeMouseMode 屬性遠端桌面服務
- RelativeMouseMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RelativeMouseMode 屬性
- RelativeMouseMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RelativeMouseMode 屬性
- RelativeMouseMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RelativeMouseMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998016"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a><span data-ttu-id="a2ac2-110">IMsRdpClientAdvancedSettings6：： RelativeMouseMode 屬性</span><span class="sxs-lookup"><span data-stu-id="a2ac2-110">IMsRdpClientAdvancedSettings6::RelativeMouseMode property</span></span>

<span data-ttu-id="a2ac2-111">指定滑鼠是否應使用相對模式。</span><span class="sxs-lookup"><span data-stu-id="a2ac2-111">Specifies whether the mouse should use relative mode.</span></span> <span data-ttu-id="a2ac2-112">如果滑鼠處於相對模式，則包含 **variant \_ TRUE** ; 如果滑鼠處於絕對模式，則為 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a2ac2-112">Contains **VARIANT\_TRUE** if the mouse is in relative mode or **VARIANT\_FALSE** if the mouse is in absolute mode.</span></span>

<span data-ttu-id="a2ac2-113">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2ac2-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ac2-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2ac2-114">Syntax</span></span>


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a><span data-ttu-id="a2ac2-115">屬性值</span><span class="sxs-lookup"><span data-stu-id="a2ac2-115">Property value</span></span>

<span data-ttu-id="a2ac2-116">包含新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="a2ac2-116">Contains the new property value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ac2-117">備註</span><span class="sxs-lookup"><span data-stu-id="a2ac2-117">Remarks</span></span>

<span data-ttu-id="a2ac2-118">滑鼠模式指出 ActiveX 控制項如何計算傳送給遠端桌面工作階段主機 (RD 工作階段主機) server 的滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="a2ac2-118">The mouse mode indicates how the ActiveX control calculates the mouse coordinates that it sends to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="a2ac2-119">當滑鼠處於相對模式時，ActiveX 控制項會計算相對於滑鼠最後一個位置的滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="a2ac2-119">When the mouse is in relative mode, the ActiveX control calculates mouse coordinates relative to the mouse's last position.</span></span> <span data-ttu-id="a2ac2-120">當滑鼠處於絕對模式時，ActiveX 控制項會計算相對於 RD 工作階段主機伺服器桌面的滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="a2ac2-120">When the mouse is in absolute mode, the ActiveX control calculates mouse coordinates relative to the desktop of the RD Session Host server.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ac2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2ac2-121">Requirements</span></span>



| <span data-ttu-id="a2ac2-122">需求</span><span class="sxs-lookup"><span data-stu-id="a2ac2-122">Requirement</span></span> | <span data-ttu-id="a2ac2-123">值</span><span class="sxs-lookup"><span data-stu-id="a2ac2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ac2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2ac2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ac2-125">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="a2ac2-125">Windows Vista with SP1</span></span><br/>                                                                |
| <span data-ttu-id="a2ac2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2ac2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ac2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2ac2-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a2ac2-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a2ac2-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2ac2-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ac2-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a2ac2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ac2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ac2-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ac2-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a2ac2-132">IID</span><span class="sxs-lookup"><span data-stu-id="a2ac2-132">IID</span></span><br/>                      | <span data-ttu-id="a2ac2-133">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="a2ac2-133">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2ac2-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2ac2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ac2-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a2ac2-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a2ac2-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a2ac2-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a2ac2-137">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a2ac2-137">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





