---
title: IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseLeft 屬性
description: 指定要新增至 Ctrl + Alt 的虛擬按鍵程式碼，以決定 Ctrl + Alt + 向左鍵的替換熱鍵。
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- HotKeyFocusReleaseLeft 屬性遠端桌面服務
- HotKeyFocusReleaseLeft 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyFocusReleaseLeft 屬性
- HotKeyFocusReleaseLeft 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyFocusReleaseLeft 屬性
- HotKeyFocusReleaseLeft 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyFocusReleaseLeft 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685534"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a><span data-ttu-id="94fbf-110">IMsRdpClientAdvancedSettings6：： HotKeyFocusReleaseLeft 屬性</span><span class="sxs-lookup"><span data-stu-id="94fbf-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft property</span></span>

<span data-ttu-id="94fbf-111">指定要新增至 Ctrl + Alt 的虛擬按鍵程式碼，以決定 Ctrl + Alt + 向左鍵的替換熱鍵。</span><span class="sxs-lookup"><span data-stu-id="94fbf-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Left Arrow.</span></span>

<span data-ttu-id="94fbf-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="94fbf-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="94fbf-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="94fbf-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a><span data-ttu-id="94fbf-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="94fbf-114">Property value</span></span>

<span data-ttu-id="94fbf-115">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="94fbf-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="94fbf-116">備註</span><span class="sxs-lookup"><span data-stu-id="94fbf-116">Remarks</span></span>

<span data-ttu-id="94fbf-117">只有遠端桌面連線6.1 和7.0 用戶端支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="94fbf-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="94fbf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="94fbf-118">Requirements</span></span>



| <span data-ttu-id="94fbf-119">需求</span><span class="sxs-lookup"><span data-stu-id="94fbf-119">Requirement</span></span> | <span data-ttu-id="94fbf-120">值</span><span class="sxs-lookup"><span data-stu-id="94fbf-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94fbf-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94fbf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94fbf-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94fbf-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="94fbf-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94fbf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94fbf-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94fbf-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="94fbf-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="94fbf-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="94fbf-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94fbf-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="94fbf-127">DLL</span><span class="sxs-lookup"><span data-stu-id="94fbf-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94fbf-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94fbf-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="94fbf-129">IID</span><span class="sxs-lookup"><span data-stu-id="94fbf-129">IID</span></span><br/>                      | <span data-ttu-id="94fbf-130">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="94fbf-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94fbf-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94fbf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fbf-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="94fbf-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="94fbf-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="94fbf-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="94fbf-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="94fbf-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





