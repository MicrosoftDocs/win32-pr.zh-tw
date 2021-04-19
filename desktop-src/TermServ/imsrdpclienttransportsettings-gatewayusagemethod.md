---
title: IMsRdpClientTransportSettings GatewayUsageMethod 屬性
description: 指定使用遠端桌面閘道 (RD 閘道) server 的時機。
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- GatewayUsageMethod 屬性遠端桌面服務
- GatewayUsageMethod 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayUsageMethod 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966097"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a><span data-ttu-id="9aec4-106">IMsRdpClientTransportSettings：： GatewayUsageMethod 屬性</span><span class="sxs-lookup"><span data-stu-id="9aec4-106">IMsRdpClientTransportSettings::GatewayUsageMethod property</span></span>

<span data-ttu-id="9aec4-107">指定使用遠端桌面閘道 (RD 閘道) server 的時機。</span><span class="sxs-lookup"><span data-stu-id="9aec4-107">Specifies when to use a Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="9aec4-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9aec4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aec4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9aec4-109">Syntax</span></span>


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="9aec4-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9aec4-110">Property value</span></span>

<span data-ttu-id="9aec4-111">指定 RD 閘道伺服器使用方法的 **ULONG** 變數。</span><span class="sxs-lookup"><span data-stu-id="9aec4-111">A **ULONG** variable that specifies the RD Gateway server usage method.</span></span> <span data-ttu-id="9aec4-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9aec4-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span data-ttu-id="9aec4-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_PROXY \_ 模式 \_ 無 \_ 直接** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="9aec4-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC\_PROXY\_MODE\_NONE\_DIRECT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9aec4-114">請勿使用 RD 閘道的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9aec4-114">Do not use an RD Gateway server.</span></span> <span data-ttu-id="9aec4-115">在遠端桌面連線 (RDC) 用戶端 UI 中，已清除 [ **本機位址略過 RD 閘道伺服器** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="9aec4-115">In the Remote Desktop Connection (RDC) client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span data-ttu-id="9aec4-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_PROXY \_ 模式 \_ 直接** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="9aec4-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC\_PROXY\_MODE\_DIRECT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="9aec4-117">一律使用 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="9aec4-117">Always use an RD Gateway server.</span></span> <span data-ttu-id="9aec4-118">在 RDC 用戶端 UI 中，[ **本機位址略過 RD 閘道伺服器** ] 核取方塊已清除。</span><span class="sxs-lookup"><span data-stu-id="9aec4-118">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span data-ttu-id="9aec4-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_PROXY \_ 模式 \_** 偵測 (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="9aec4-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC\_PROXY\_MODE\_DETECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="9aec4-120">如果無法直接連接到 RD 工作階段主機伺服器，請使用 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="9aec4-120">Use an RD Gateway server if a direct connection cannot be made to the RD Session Host server.</span></span> <span data-ttu-id="9aec4-121">在 RDC 用戶端 UI 中，已選取 [ **略過本機位址的 RD 閘道伺服器** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="9aec4-121">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span data-ttu-id="9aec4-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_PROXY \_ 模式 \_ 預設** (3 (0x3) ) </span><span class="sxs-lookup"><span data-stu-id="9aec4-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC\_PROXY\_MODE\_DEFAULT** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="9aec4-123">使用預設 RD 閘道伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="9aec4-123">Use the default RD Gateway server settings.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span data-ttu-id="9aec4-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_PROXY \_ 模式 \_ NONE \_** 偵測 (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="9aec4-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC\_PROXY\_MODE\_NONE\_DETECT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="9aec4-125">請勿使用 RD 閘道的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9aec4-125">Do not use an RD Gateway server.</span></span> <span data-ttu-id="9aec4-126">在 RDC 用戶端 UI 中，已選取 [ **略過本機位址的 RD 閘道伺服器** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="9aec4-126">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="9aec4-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9aec4-127">Error codes</span></span>

<span data-ttu-id="9aec4-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="9aec4-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aec4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9aec4-129">Requirements</span></span>



| <span data-ttu-id="9aec4-130">需求</span><span class="sxs-lookup"><span data-stu-id="9aec4-130">Requirement</span></span> | <span data-ttu-id="9aec4-131">值</span><span class="sxs-lookup"><span data-stu-id="9aec4-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aec4-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9aec4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9aec4-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9aec4-133">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="9aec4-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9aec4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9aec4-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aec4-135">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="9aec4-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9aec4-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="9aec4-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aec4-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9aec4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9aec4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aec4-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aec4-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9aec4-140">IID</span><span class="sxs-lookup"><span data-stu-id="9aec4-140">IID</span></span><br/>                      | <span data-ttu-id="9aec4-141">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="9aec4-141">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9aec4-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9aec4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aec4-143">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="9aec4-143">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





