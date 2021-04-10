---
title: IMsRdpClientAdvancedSettings6 AuthenticationType 屬性
description: 指定用於此連接的驗證類型。
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- AuthenticationType 屬性遠端桌面服務
- AuthenticationType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，AuthenticationType 屬性
- AuthenticationType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AuthenticationType 屬性
- AuthenticationType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AuthenticationType 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103691"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a><span data-ttu-id="4203f-110">IMsRdpClientAdvancedSettings6：： AuthenticationType 屬性</span><span class="sxs-lookup"><span data-stu-id="4203f-110">IMsRdpClientAdvancedSettings6::AuthenticationType property</span></span>

<span data-ttu-id="4203f-111">指定用於此連接的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="4203f-111">Specifies the type of authentication used for this connection.</span></span>

<span data-ttu-id="4203f-112">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4203f-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4203f-113">語法</span><span class="sxs-lookup"><span data-stu-id="4203f-113">Syntax</span></span>


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a><span data-ttu-id="4203f-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="4203f-114">Property value</span></span>

<span data-ttu-id="4203f-115">接收指定用於此連接之驗證類型的值。</span><span class="sxs-lookup"><span data-stu-id="4203f-115">Receives a value that specifies the type of authentication used for this connection.</span></span> <span data-ttu-id="4203f-116">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4203f-116">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="4203f-117">0</span><span class="sxs-lookup"><span data-stu-id="4203f-117">0</span></span>
</dt> <dd>

<span data-ttu-id="4203f-118">未使用任何驗證。</span><span class="sxs-lookup"><span data-stu-id="4203f-118">No authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="4203f-119">1</span><span class="sxs-lookup"><span data-stu-id="4203f-119">1</span></span>
</dt> <dd>

<span data-ttu-id="4203f-120">使用憑證驗證。</span><span class="sxs-lookup"><span data-stu-id="4203f-120">Certificate authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="4203f-121">2</span><span class="sxs-lookup"><span data-stu-id="4203f-121">2</span></span>
</dt> <dd>

<span data-ttu-id="4203f-122">使用 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="4203f-122">Kerberos authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="4203f-123">3</span><span class="sxs-lookup"><span data-stu-id="4203f-123">3</span></span>
</dt> <dd>

<span data-ttu-id="4203f-124">使用憑證和 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="4203f-124">Both certificate and Kerberos authentication are used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4203f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4203f-125">Requirements</span></span>



| <span data-ttu-id="4203f-126">需求</span><span class="sxs-lookup"><span data-stu-id="4203f-126">Requirement</span></span> | <span data-ttu-id="4203f-127">值</span><span class="sxs-lookup"><span data-stu-id="4203f-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4203f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4203f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4203f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4203f-129">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="4203f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4203f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4203f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4203f-131">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="4203f-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4203f-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="4203f-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4203f-133"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4203f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4203f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4203f-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4203f-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4203f-136">IID</span><span class="sxs-lookup"><span data-stu-id="4203f-136">IID</span></span><br/>                      | <span data-ttu-id="4203f-137">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="4203f-137">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4203f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4203f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4203f-139">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4203f-139">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4203f-140">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4203f-140">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4203f-141">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4203f-141">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





