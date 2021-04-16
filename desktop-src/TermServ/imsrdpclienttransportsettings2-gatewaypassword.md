---
title: IMsRdpClientTransportSettings2 GatewayPassword 屬性
description: 指定使用者提供的密碼，以連接到遠端桌面閘道 (RD 閘道) server。
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- GatewayPassword 屬性遠端桌面服務
- GatewayPassword 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayPassword 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508380"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a><span data-ttu-id="33d85-106">IMsRdpClientTransportSettings2：： GatewayPassword 屬性</span><span class="sxs-lookup"><span data-stu-id="33d85-106">IMsRdpClientTransportSettings2::GatewayPassword property</span></span>

<span data-ttu-id="33d85-107">指定使用者提供的密碼，以連接到遠端桌面閘道 (RD 閘道) server。</span><span class="sxs-lookup"><span data-stu-id="33d85-107">Specifies the password that a user provides to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="33d85-108">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="33d85-108">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d85-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="33d85-109">Syntax</span></span>


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a><span data-ttu-id="33d85-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="33d85-110">Property value</span></span>

<span data-ttu-id="33d85-111">使用者為了連接到 RD 閘道伺服器所提供的密碼。</span><span class="sxs-lookup"><span data-stu-id="33d85-111">The password that a user provides to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="33d85-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="33d85-112">Error codes</span></span>

<span data-ttu-id="33d85-113">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="33d85-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="33d85-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="33d85-114">Requirements</span></span>



| <span data-ttu-id="33d85-115">需求</span><span class="sxs-lookup"><span data-stu-id="33d85-115">Requirement</span></span> | <span data-ttu-id="33d85-116">值</span><span class="sxs-lookup"><span data-stu-id="33d85-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33d85-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33d85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33d85-118">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="33d85-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="33d85-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33d85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33d85-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33d85-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="33d85-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="33d85-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="33d85-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33d85-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="33d85-123">DLL</span><span class="sxs-lookup"><span data-stu-id="33d85-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33d85-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33d85-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="33d85-125">IID</span><span class="sxs-lookup"><span data-stu-id="33d85-125">IID</span></span><br/>                      | <span data-ttu-id="33d85-126">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="33d85-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33d85-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33d85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d85-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="33d85-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="33d85-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="33d85-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





