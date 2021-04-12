---
title: IMsRdpClientTransportSettings GatewayCredsSource 屬性
description: 指定或抓取遠端桌面閘道 (RD 閘道) 驗證方法。
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- GatewayCredsSource 屬性遠端桌面服務
- GatewayCredsSource 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayCredsSource 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384174"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a><span data-ttu-id="88cd9-106">IMsRdpClientTransportSettings：： GatewayCredsSource 屬性</span><span class="sxs-lookup"><span data-stu-id="88cd9-106">IMsRdpClientTransportSettings::GatewayCredsSource property</span></span>

<span data-ttu-id="88cd9-107">指定或抓取遠端桌面閘道 (RD 閘道) 驗證方法。</span><span class="sxs-lookup"><span data-stu-id="88cd9-107">Specifies or retrieves the Remote Desktop Gateway (RD Gateway) authentication method.</span></span>

<span data-ttu-id="88cd9-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="88cd9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="88cd9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="88cd9-109">Syntax</span></span>


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="88cd9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="88cd9-110">Property value</span></span>

<span data-ttu-id="88cd9-111">指定 RD 閘道驗證方法的 **ULONG** 變數。</span><span class="sxs-lookup"><span data-stu-id="88cd9-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="88cd9-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="88cd9-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="88cd9-113">TSC \_ PROXY \_ 認證 \_ 模式 \_ USERPASS (0) </span><span class="sxs-lookup"><span data-stu-id="88cd9-113">TSC\_PROXY\_CREDS\_MODE\_USERPASS (0)</span></span>
</dt> <dd>

<span data-ttu-id="88cd9-114">使用 (NTLM) 的密碼做為 RD 閘道的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="88cd9-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="88cd9-115">TSC \_ PROXY \_ 認證 \_ 模式 \_ 智慧卡 (1) </span><span class="sxs-lookup"><span data-stu-id="88cd9-115">TSC\_PROXY\_CREDS\_MODE\_SMARTCARD (1)</span></span>
</dt> <dd>

<span data-ttu-id="88cd9-116">使用智慧卡做為 RD 閘道的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="88cd9-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="88cd9-117">\_ \_ \_ \_ 所有 (4) 的 TSC PROXY 認證模式</span><span class="sxs-lookup"><span data-stu-id="88cd9-117">TSC\_PROXY\_CREDS\_MODE\_ANY (4)</span></span>
</dt> <dd>

<span data-ttu-id="88cd9-118">針對 RD 閘道使用任何驗證方法。</span><span class="sxs-lookup"><span data-stu-id="88cd9-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="88cd9-119">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="88cd9-119">Error codes</span></span>

<span data-ttu-id="88cd9-120">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="88cd9-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="88cd9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="88cd9-121">Requirements</span></span>



| <span data-ttu-id="88cd9-122">需求</span><span class="sxs-lookup"><span data-stu-id="88cd9-122">Requirement</span></span> | <span data-ttu-id="88cd9-123">值</span><span class="sxs-lookup"><span data-stu-id="88cd9-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88cd9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88cd9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88cd9-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88cd9-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="88cd9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88cd9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88cd9-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88cd9-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="88cd9-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="88cd9-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="88cd9-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88cd9-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="88cd9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="88cd9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88cd9-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88cd9-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="88cd9-132">IID</span><span class="sxs-lookup"><span data-stu-id="88cd9-132">IID</span></span><br/>                      | <span data-ttu-id="88cd9-133">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="88cd9-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88cd9-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88cd9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cd9-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="88cd9-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





