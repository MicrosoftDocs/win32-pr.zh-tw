---
title: IMsRdpClientAdvancedSettings6 EnableCredSspSupport 屬性
description: 指定是否為此連線啟用 (CredSSP) 的認證安全性服務提供者。
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- EnableCredSspSupport 屬性遠端桌面服務
- EnableCredSspSupport 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，EnableCredSspSupport 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508560"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a><span data-ttu-id="7aec6-110">IMsRdpClientAdvancedSettings6：： EnableCredSspSupport 屬性</span><span class="sxs-lookup"><span data-stu-id="7aec6-110">IMsRdpClientAdvancedSettings6::EnableCredSspSupport property</span></span>

<span data-ttu-id="7aec6-111">指定是否為此連線啟用 (CredSSP) 的認證安全性服務提供者。</span><span class="sxs-lookup"><span data-stu-id="7aec6-111">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="7aec6-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="7aec6-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aec6-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aec6-113">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="7aec6-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="7aec6-114">Property value</span></span>

<span data-ttu-id="7aec6-115">指定是否啟用此連接的 CredSSP。</span><span class="sxs-lookup"><span data-stu-id="7aec6-115">Specifies whether CredSSP is enabled for this connection.</span></span> <span data-ttu-id="7aec6-116">如果設定為 **VARIANT \_ TRUE，則** 啟用 CredSSP 或 variant FALSE，否則為 **\_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7aec6-116">Set to **VARIANT\_TRUE** to enable CredSSP or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aec6-117">備註</span><span class="sxs-lookup"><span data-stu-id="7aec6-117">Remarks</span></span>

<span data-ttu-id="7aec6-118">只有遠端桌面連線6.1 和7.0 用戶端支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="7aec6-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aec6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7aec6-119">Requirements</span></span>



| <span data-ttu-id="7aec6-120">需求</span><span class="sxs-lookup"><span data-stu-id="7aec6-120">Requirement</span></span> | <span data-ttu-id="7aec6-121">值</span><span class="sxs-lookup"><span data-stu-id="7aec6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aec6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7aec6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7aec6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7aec6-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="7aec6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7aec6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7aec6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7aec6-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="7aec6-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7aec6-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="7aec6-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aec6-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7aec6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7aec6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aec6-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aec6-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7aec6-130">IID</span><span class="sxs-lookup"><span data-stu-id="7aec6-130">IID</span></span><br/>                      | <span data-ttu-id="7aec6-131">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="7aec6-131">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7aec6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7aec6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aec6-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7aec6-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7aec6-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7aec6-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7aec6-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7aec6-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





