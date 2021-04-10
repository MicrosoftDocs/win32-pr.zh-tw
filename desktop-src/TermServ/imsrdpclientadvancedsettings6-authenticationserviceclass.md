---
title: IMsRdpClientAdvancedSettings6 AuthenticationServiceClass 屬性
description: 指定服務主體名稱 (SPN) 用來向伺服器進行驗證。
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- AuthenticationServiceClass 屬性遠端桌面服務
- AuthenticationServiceClass 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，AuthenticationServiceClass 屬性
- AuthenticationServiceClass 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AuthenticationServiceClass 屬性
- AuthenticationServiceClass 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AuthenticationServiceClass 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685912"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a><span data-ttu-id="a5965-110">IMsRdpClientAdvancedSettings6：： AuthenticationServiceClass 屬性</span><span class="sxs-lookup"><span data-stu-id="a5965-110">IMsRdpClientAdvancedSettings6::AuthenticationServiceClass property</span></span>

<span data-ttu-id="a5965-111">指定服務主體名稱 (SPN) 用來向伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="a5965-111">Specifies the service principal name (SPN) to use for authentication to the server.</span></span>

<span data-ttu-id="a5965-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a5965-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5965-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5965-113">Syntax</span></span>


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a><span data-ttu-id="a5965-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="a5965-114">Property value</span></span>

<span data-ttu-id="a5965-115">指定要使用的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="a5965-115">Specifies the service principal name to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5965-116">備註</span><span class="sxs-lookup"><span data-stu-id="a5965-116">Remarks</span></span>

<span data-ttu-id="a5965-117">只有遠端桌面連線6.1 和7.0 用戶端支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="a5965-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="a5965-118">服務主體名稱 (Spn) 與服務執行所在的安全性內容 (使用者或群組) 相關聯的安全性主體。</span><span class="sxs-lookup"><span data-stu-id="a5965-118">Service principal names (SPNs) are associated with the security principal (user or groups) in whose security context the service executes.</span></span> <span data-ttu-id="a5965-119">Spn 是用來支援用戶端應用程式與服務之間的相互驗證。</span><span class="sxs-lookup"><span data-stu-id="a5965-119">SPNs are used to support mutual authentication between a client application and a service.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5965-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5965-120">Requirements</span></span>



| <span data-ttu-id="a5965-121">需求</span><span class="sxs-lookup"><span data-stu-id="a5965-121">Requirement</span></span> | <span data-ttu-id="a5965-122">值</span><span class="sxs-lookup"><span data-stu-id="a5965-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5965-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5965-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a5965-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5965-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a5965-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5965-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a5965-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5965-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a5965-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a5965-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5965-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5965-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a5965-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a5965-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5965-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5965-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a5965-131">IID</span><span class="sxs-lookup"><span data-stu-id="a5965-131">IID</span></span><br/>                      | <span data-ttu-id="a5965-132">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="a5965-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5965-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5965-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5965-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a5965-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a5965-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a5965-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a5965-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a5965-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





