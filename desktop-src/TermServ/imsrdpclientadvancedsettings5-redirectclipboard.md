---
title: IMsRdpClientAdvancedSettings5 RedirectClipboard 屬性
description: 設定或抓取剪貼簿重新導向的設定。
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- RedirectClipboard 屬性遠端桌面服務
- RedirectClipboard 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RedirectClipboard 屬性
- RedirectClipboard 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RedirectClipboard 屬性
- RedirectClipboard 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RedirectClipboard 屬性
- RedirectClipboard 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RedirectClipboard 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aba9950b8d602ca239d66364279a5876a432d04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934127"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a><span data-ttu-id="65356-112">IMsRdpClientAdvancedSettings5：： RedirectClipboard 屬性</span><span class="sxs-lookup"><span data-stu-id="65356-112">IMsRdpClientAdvancedSettings5::RedirectClipboard property</span></span>

<span data-ttu-id="65356-113">設定或抓取剪貼簿重新導向的設定。</span><span class="sxs-lookup"><span data-stu-id="65356-113">Sets or retrieves the configuration for clipboard redirection.</span></span>

<span data-ttu-id="65356-114">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="65356-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65356-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="65356-115">Syntax</span></span>


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a><span data-ttu-id="65356-116">屬性值</span><span class="sxs-lookup"><span data-stu-id="65356-116">Property value</span></span>

<span data-ttu-id="65356-117">將剪貼簿重新導向模式設定為 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="65356-117">Sets the clipboard redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="65356-118">如果設定為 **TRUE**，則會啟用剪貼簿重新導向模式。</span><span class="sxs-lookup"><span data-stu-id="65356-118">If set to **TRUE**, clipboard redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="65356-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="65356-119">Requirements</span></span>



| <span data-ttu-id="65356-120">需求</span><span class="sxs-lookup"><span data-stu-id="65356-120">Requirement</span></span> | <span data-ttu-id="65356-121">值</span><span class="sxs-lookup"><span data-stu-id="65356-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65356-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65356-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65356-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65356-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="65356-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65356-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65356-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65356-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="65356-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="65356-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="65356-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65356-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65356-128">DLL</span><span class="sxs-lookup"><span data-stu-id="65356-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65356-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65356-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65356-130">IID</span><span class="sxs-lookup"><span data-stu-id="65356-130">IID</span></span><br/>                      | <span data-ttu-id="65356-131">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="65356-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65356-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65356-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65356-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="65356-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="65356-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="65356-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="65356-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65356-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="65356-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="65356-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





