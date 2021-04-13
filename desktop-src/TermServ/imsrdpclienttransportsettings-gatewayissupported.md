---
title: IMsRdpClientTransportSettings GatewayIsSupported 屬性
description: 指定是否支援遠端桌面閘道 (RD 閘道) 。
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- GatewayIsSupported 屬性遠端桌面服務
- GatewayIsSupported 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayIsSupported 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383885"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a><span data-ttu-id="1fbf2-106">IMsRdpClientTransportSettings：： GatewayIsSupported 屬性</span><span class="sxs-lookup"><span data-stu-id="1fbf2-106">IMsRdpClientTransportSettings::GatewayIsSupported property</span></span>

<span data-ttu-id="1fbf2-107">指定是否支援遠端桌面閘道 (RD 閘道) 。</span><span class="sxs-lookup"><span data-stu-id="1fbf2-107">Specifies whether Remote Desktop Gateway (RD Gateway) is supported.</span></span>

<span data-ttu-id="1fbf2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1fbf2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fbf2-109">語法</span><span class="sxs-lookup"><span data-stu-id="1fbf2-109">Syntax</span></span>


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a><span data-ttu-id="1fbf2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="1fbf2-110">Property value</span></span>

<span data-ttu-id="1fbf2-111">指定是否支援 RD 閘道。</span><span class="sxs-lookup"><span data-stu-id="1fbf2-111">Specifies whether RD Gateway is supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1fbf2-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1fbf2-112">Error codes</span></span>

<span data-ttu-id="1fbf2-113">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="1fbf2-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fbf2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fbf2-114">Requirements</span></span>



| <span data-ttu-id="1fbf2-115">需求</span><span class="sxs-lookup"><span data-stu-id="1fbf2-115">Requirement</span></span> | <span data-ttu-id="1fbf2-116">值</span><span class="sxs-lookup"><span data-stu-id="1fbf2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fbf2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fbf2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1fbf2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fbf2-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1fbf2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fbf2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1fbf2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fbf2-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1fbf2-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1fbf2-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1fbf2-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fbf2-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1fbf2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1fbf2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fbf2-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fbf2-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1fbf2-125">IID</span><span class="sxs-lookup"><span data-stu-id="1fbf2-125">IID</span></span><br/>                      | <span data-ttu-id="1fbf2-126">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="1fbf2-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fbf2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fbf2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fbf2-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="1fbf2-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





