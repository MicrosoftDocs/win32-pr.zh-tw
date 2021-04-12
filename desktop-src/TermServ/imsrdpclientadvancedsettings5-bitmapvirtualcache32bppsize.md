---
title: IMsRdpClientAdvancedSettings5 BitmapVirtualCache32BppSize 屬性
description: 設定或抓取每圖元32位的虛擬快取檔案大小 (bpp) 點陣圖。
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCache32BppSize 屬性遠端桌面服務
- BitmapVirtualCache32BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，BitmapVirtualCache32BppSize 屬性
- BitmapVirtualCache32BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，BitmapVirtualCache32BppSize 屬性
- BitmapVirtualCache32BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，BitmapVirtualCache32BppSize 屬性
- BitmapVirtualCache32BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BitmapVirtualCache32BppSize 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384298"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a><span data-ttu-id="d60fb-112">IMsRdpClientAdvancedSettings5：： BitmapVirtualCache32BppSize 屬性</span><span class="sxs-lookup"><span data-stu-id="d60fb-112">IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize property</span></span>

<span data-ttu-id="d60fb-113">設定或抓取每圖元32位的虛擬快取檔案大小 (bpp) 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d60fb-113">Sets or retrieves the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span>

<span data-ttu-id="d60fb-114">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d60fb-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d60fb-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="d60fb-115">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="d60fb-116">屬性值</span><span class="sxs-lookup"><span data-stu-id="d60fb-116">Property value</span></span>

<span data-ttu-id="d60fb-117">設定 32 bpp 點陣圖的虛擬快取檔案大小，以 mb (MB) 。</span><span class="sxs-lookup"><span data-stu-id="d60fb-117">Sets the size of the virtual cache file for 32 bpp bitmaps, in megabytes (MB).</span></span> <span data-ttu-id="d60fb-118">最大值為 48 MB。</span><span class="sxs-lookup"><span data-stu-id="d60fb-118">The maximum value is 48 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="d60fb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d60fb-119">Requirements</span></span>



| <span data-ttu-id="d60fb-120">需求</span><span class="sxs-lookup"><span data-stu-id="d60fb-120">Requirement</span></span> | <span data-ttu-id="d60fb-121">值</span><span class="sxs-lookup"><span data-stu-id="d60fb-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d60fb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d60fb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d60fb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d60fb-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="d60fb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d60fb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d60fb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d60fb-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="d60fb-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d60fb-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d60fb-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d60fb-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d60fb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d60fb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d60fb-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d60fb-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d60fb-130">IID</span><span class="sxs-lookup"><span data-stu-id="d60fb-130">IID</span></span><br/>                      | <span data-ttu-id="d60fb-131">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="d60fb-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d60fb-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d60fb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d60fb-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d60fb-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d60fb-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d60fb-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d60fb-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d60fb-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d60fb-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d60fb-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





