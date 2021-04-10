---
title: IMsRdpClientAdvancedSettings7 EnableSuperPan 屬性
description: 指定或抓取布林值，指出 SuperPan 是否已啟用或停用。
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- EnableSuperPan 屬性遠端桌面服務
- EnableSuperPan 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，EnableSuperPan 屬性
- EnableSuperPan 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，EnableSuperPan 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686066"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a><span data-ttu-id="2574d-108">IMsRdpClientAdvancedSettings7：： EnableSuperPan 屬性</span><span class="sxs-lookup"><span data-stu-id="2574d-108">IMsRdpClientAdvancedSettings7::EnableSuperPan property</span></span>

<span data-ttu-id="2574d-109">指定或抓取布林值，指出 SuperPan 是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="2574d-109">Specifies or retrieves a Boolean value that indicates whether SuperPan is enabled or disabled.</span></span> <span data-ttu-id="2574d-110">SuperPan 是一項功能，可讓使用者在遠端桌面的維度大於目前用戶端視窗的維度時，輕鬆地在全螢幕模式下流覽遠端桌面。</span><span class="sxs-lookup"><span data-stu-id="2574d-110">SuperPan is a feature that allows a user to easily navigate a remote desktop in full-screen mode, when the dimensions of the remote desktop are larger than the dimensions of the current client window.</span></span> <span data-ttu-id="2574d-111">使用者可以指向視窗框線，而不是使用捲軸來流覽桌面，而是讓遠端桌面自動在該方向中滾動。</span><span class="sxs-lookup"><span data-stu-id="2574d-111">Instead of using scroll bars to navigate the desktop, the user can point to the window border, and the remote desktop will scroll automatically in that direction.</span></span> <span data-ttu-id="2574d-112">SuperPan 不支援一個以上的監視器。</span><span class="sxs-lookup"><span data-stu-id="2574d-112">SuperPan does not support more than one monitor.</span></span>

<span data-ttu-id="2574d-113">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2574d-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2574d-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="2574d-114">Syntax</span></span>


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a><span data-ttu-id="2574d-115">屬性值</span><span class="sxs-lookup"><span data-stu-id="2574d-115">Property value</span></span>

<span data-ttu-id="2574d-116">**VARIANT \_ BOOL** 值，指定是否啟用 SuperPan。</span><span class="sxs-lookup"><span data-stu-id="2574d-116">A **VARIANT\_BOOL** value that specifies whether SuperPan is enabled.</span></span> <span data-ttu-id="2574d-117">**VARIANT \_ TRUE** 值指定啟用 SuperPan。</span><span class="sxs-lookup"><span data-stu-id="2574d-117">A value of **VARIANT\_TRUE** specifies that SuperPan is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2574d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2574d-118">Requirements</span></span>



| <span data-ttu-id="2574d-119">需求</span><span class="sxs-lookup"><span data-stu-id="2574d-119">Requirement</span></span> | <span data-ttu-id="2574d-120">值</span><span class="sxs-lookup"><span data-stu-id="2574d-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2574d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2574d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2574d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2574d-122">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="2574d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2574d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2574d-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2574d-124">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="2574d-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2574d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="2574d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2574d-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2574d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2574d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2574d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2574d-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2574d-129">IID</span><span class="sxs-lookup"><span data-stu-id="2574d-129">IID</span></span><br/>                      | <span data-ttu-id="2574d-130">IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="2574d-130">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2574d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2574d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2574d-132">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2574d-132">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2574d-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2574d-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





