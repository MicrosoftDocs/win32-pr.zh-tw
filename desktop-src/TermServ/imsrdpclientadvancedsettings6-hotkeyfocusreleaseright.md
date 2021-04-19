---
title: IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseRight 屬性
description: 指定要新增至 Ctrl + Alt 的虛擬按鍵程式碼，以決定 Ctrl + Alt + 向右鍵的熱鍵取代。
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- HotKeyFocusReleaseRight 屬性遠端桌面服務
- HotKeyFocusReleaseRight 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyFocusReleaseRight 屬性
- HotKeyFocusReleaseRight 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyFocusReleaseRight 屬性
- HotKeyFocusReleaseRight 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyFocusReleaseRight 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106988039"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a><span data-ttu-id="72f94-110">IMsRdpClientAdvancedSettings6：： HotKeyFocusReleaseRight 屬性</span><span class="sxs-lookup"><span data-stu-id="72f94-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight property</span></span>

<span data-ttu-id="72f94-111">指定要新增至 Ctrl + Alt 的虛擬按鍵程式碼，以決定 Ctrl + Alt + 向右鍵的熱鍵取代。</span><span class="sxs-lookup"><span data-stu-id="72f94-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Right Arrow.</span></span>

<span data-ttu-id="72f94-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="72f94-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f94-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="72f94-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a><span data-ttu-id="72f94-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="72f94-114">Property value</span></span>

<span data-ttu-id="72f94-115">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="72f94-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f94-116">備註</span><span class="sxs-lookup"><span data-stu-id="72f94-116">Remarks</span></span>

<span data-ttu-id="72f94-117">只有遠端桌面連線6.1 和7.0 用戶端支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="72f94-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f94-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="72f94-118">Requirements</span></span>



| <span data-ttu-id="72f94-119">需求</span><span class="sxs-lookup"><span data-stu-id="72f94-119">Requirement</span></span> | <span data-ttu-id="72f94-120">值</span><span class="sxs-lookup"><span data-stu-id="72f94-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f94-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72f94-121">Minimum supported client</span></span><br/> | <span data-ttu-id="72f94-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72f94-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="72f94-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72f94-123">Minimum supported server</span></span><br/> | <span data-ttu-id="72f94-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72f94-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="72f94-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="72f94-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="72f94-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f94-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="72f94-127">DLL</span><span class="sxs-lookup"><span data-stu-id="72f94-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72f94-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f94-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="72f94-129">IID</span><span class="sxs-lookup"><span data-stu-id="72f94-129">IID</span></span><br/>                      | <span data-ttu-id="72f94-130">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="72f94-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72f94-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72f94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f94-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="72f94-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="72f94-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="72f94-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="72f94-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="72f94-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





