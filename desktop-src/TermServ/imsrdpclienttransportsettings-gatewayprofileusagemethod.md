---
title: IMsRdpClientTransportSettings GatewayProfileUsageMethod 屬性
description: 指定是否要使用預設遠端桌面閘道 (RD 閘道) 設定。
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- GatewayProfileUsageMethod 屬性遠端桌面服務
- GatewayProfileUsageMethod 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayProfileUsageMethod 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384585"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a><span data-ttu-id="caf72-106">IMsRdpClientTransportSettings：： GatewayProfileUsageMethod 屬性</span><span class="sxs-lookup"><span data-stu-id="caf72-106">IMsRdpClientTransportSettings::GatewayProfileUsageMethod property</span></span>

<span data-ttu-id="caf72-107">指定是否要使用預設遠端桌面閘道 (RD 閘道) 設定。</span><span class="sxs-lookup"><span data-stu-id="caf72-107">Specifies whether to use default Remote Desktop Gateway (RD Gateway) settings.</span></span>

<span data-ttu-id="caf72-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="caf72-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf72-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="caf72-109">Syntax</span></span>


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="caf72-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="caf72-110">Property value</span></span>

<span data-ttu-id="caf72-111">RD 閘道設定檔使用方法。</span><span class="sxs-lookup"><span data-stu-id="caf72-111">The RD Gateway profile usage method.</span></span> <span data-ttu-id="caf72-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="caf72-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span data-ttu-id="caf72-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_PROXY \_ 設定檔 \_ 模式 \_ 預設** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="caf72-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC\_PROXY\_PROFILE\_MODE\_DEFAULT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="caf72-114">使用系統管理員所指定的預設配置檔案模式。</span><span class="sxs-lookup"><span data-stu-id="caf72-114">Use the default profile mode, as specified by the administrator.</span></span>

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span data-ttu-id="caf72-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_PROXY \_ 設定檔 \_ 模式 \_ 明確** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="caf72-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC\_PROXY\_PROFILE\_MODE\_EXPLICIT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="caf72-116">使用明確的設定，如使用者所指定。</span><span class="sxs-lookup"><span data-stu-id="caf72-116">Use explicit settings, as specified by the user.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="caf72-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="caf72-117">Error codes</span></span>

<span data-ttu-id="caf72-118">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="caf72-118">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf72-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="caf72-119">Requirements</span></span>



| <span data-ttu-id="caf72-120">需求</span><span class="sxs-lookup"><span data-stu-id="caf72-120">Requirement</span></span> | <span data-ttu-id="caf72-121">值</span><span class="sxs-lookup"><span data-stu-id="caf72-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf72-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caf72-122">Minimum supported client</span></span><br/> | <span data-ttu-id="caf72-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="caf72-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="caf72-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caf72-124">Minimum supported server</span></span><br/> | <span data-ttu-id="caf72-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="caf72-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="caf72-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="caf72-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="caf72-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caf72-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="caf72-128">DLL</span><span class="sxs-lookup"><span data-stu-id="caf72-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caf72-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caf72-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="caf72-130">IID</span><span class="sxs-lookup"><span data-stu-id="caf72-130">IID</span></span><br/>                      | <span data-ttu-id="caf72-131">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="caf72-131">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="caf72-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caf72-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf72-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="caf72-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





