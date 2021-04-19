---
title: IMsRdpClientTransportSettings GatewayDefaultUsageMethod 屬性
description: 遠端桌面閘道 (RD 閘道) 的預設使用方法。
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- GatewayDefaultUsageMethod 屬性遠端桌面服務
- GatewayDefaultUsageMethod 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayDefaultUsageMethod 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979679"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a><span data-ttu-id="cb640-106">IMsRdpClientTransportSettings：： GatewayDefaultUsageMethod 屬性</span><span class="sxs-lookup"><span data-stu-id="cb640-106">IMsRdpClientTransportSettings::GatewayDefaultUsageMethod property</span></span>

<span data-ttu-id="cb640-107">遠端桌面閘道 (RD 閘道) 的預設使用方法。</span><span class="sxs-lookup"><span data-stu-id="cb640-107">The default usage method for Remote Desktop Gateway (RD Gateway).</span></span>

<span data-ttu-id="cb640-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cb640-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb640-109">語法</span><span class="sxs-lookup"><span data-stu-id="cb640-109">Syntax</span></span>


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="cb640-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="cb640-110">Property value</span></span>

<span data-ttu-id="cb640-111">RD 閘道之預設使用方法的指標。</span><span class="sxs-lookup"><span data-stu-id="cb640-111">A pointer to the default usage method for RD Gateway.</span></span> <span data-ttu-id="cb640-112">傳回 [**put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)和群組原則設定所設定之使用者設定的聯集。</span><span class="sxs-lookup"><span data-stu-id="cb640-112">Returns a union of the user settings that are set by [**put\_GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md), and group policy settings.</span></span> <span data-ttu-id="cb640-113">如果 **put \_ GatewayUsageMethod ()** 沒有設定任何使用者設定， **get \_ GatewayDefaultUsageMethod ()** 將會傳回 [ **TSC \_ PROXY 模式偵測 \_ ] \_** 的預設值。</span><span class="sxs-lookup"><span data-stu-id="cb640-113">If no user settings were set by **put\_GatewayUsageMethod()**, **get\_GatewayDefaultUsageMethod()** will return the default value of **TSC\_PROXY\_MODE\_DETECT**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb640-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cb640-114">Error codes</span></span>

<span data-ttu-id="cb640-115">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="cb640-115">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb640-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb640-116">Requirements</span></span>



| <span data-ttu-id="cb640-117">需求</span><span class="sxs-lookup"><span data-stu-id="cb640-117">Requirement</span></span> | <span data-ttu-id="cb640-118">值</span><span class="sxs-lookup"><span data-stu-id="cb640-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb640-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb640-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb640-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb640-120">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="cb640-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb640-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb640-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb640-122">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="cb640-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="cb640-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb640-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb640-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cb640-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cb640-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb640-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb640-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cb640-127">IID</span><span class="sxs-lookup"><span data-stu-id="cb640-127">IID</span></span><br/>                      | <span data-ttu-id="cb640-128">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="cb640-128">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb640-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb640-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb640-130">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="cb640-130">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





