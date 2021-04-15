---
title: IMsRdpClientTransportSettings GatewayUserSelectedCredsSource 屬性
description: 設定或抓取使用者指定的遠端桌面閘道 (RD 閘道) 認證來源。
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- GatewayUserSelectedCredsSource 屬性遠端桌面服務
- GatewayUserSelectedCredsSource 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayUserSelectedCredsSource 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508383"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a><span data-ttu-id="5e5fb-106">IMsRdpClientTransportSettings：： GatewayUserSelectedCredsSource 屬性</span><span class="sxs-lookup"><span data-stu-id="5e5fb-106">IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource property</span></span>

<span data-ttu-id="5e5fb-107">設定或抓取使用者指定的遠端桌面閘道 (RD 閘道) 認證來源。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-107">Sets or retrieves the user-specified Remote Desktop Gateway (RD Gateway) credential source.</span></span>

<span data-ttu-id="5e5fb-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5fb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e5fb-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="5e5fb-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5e5fb-110">Property value</span></span>

<span data-ttu-id="5e5fb-111">指定 RD 閘道驗證方法的 **ULONG** 變數。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="5e5fb-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span data-ttu-id="5e5fb-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_PROXY \_ 認證 \_ 模式 \_ USERPASS** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="5e5fb-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC\_PROXY\_CREDS\_MODE\_USERPASS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5e5fb-114">使用 (NTLM) 的密碼做為 RD 閘道的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span data-ttu-id="5e5fb-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_PROXY \_ 認證 \_ 模式 \_ 智慧卡** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="5e5fb-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC\_PROXY\_CREDS\_MODE\_SMARTCARD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5e5fb-116">使用智慧卡做為 RD 閘道的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span data-ttu-id="5e5fb-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_PROXY \_ 認證 \_ 模式 \_ 任何** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="5e5fb-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC\_PROXY\_CREDS\_MODE\_ANY** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="5e5fb-118">針對 RD 閘道使用任何驗證方法。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="5e5fb-119">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5e5fb-119">Error codes</span></span>

<span data-ttu-id="5e5fb-120">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="5e5fb-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5fb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e5fb-121">Requirements</span></span>



| <span data-ttu-id="5e5fb-122">需求</span><span class="sxs-lookup"><span data-stu-id="5e5fb-122">Requirement</span></span> | <span data-ttu-id="5e5fb-123">值</span><span class="sxs-lookup"><span data-stu-id="5e5fb-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5fb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e5fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5fb-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e5fb-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="5e5fb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e5fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5fb-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e5fb-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="5e5fb-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5e5fb-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e5fb-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e5fb-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5e5fb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5e5fb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5fb-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e5fb-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5e5fb-132">IID</span><span class="sxs-lookup"><span data-stu-id="5e5fb-132">IID</span></span><br/>                      | <span data-ttu-id="5e5fb-133">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="5e5fb-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e5fb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e5fb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5fb-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="5e5fb-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





