---
title: IMsRdpClientTransportSettings2 GatewayDomain 屬性
description: 指定或抓取提供給遠端桌面閘道 (RD 閘道) 伺服器之使用者的功能變數名稱。
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- GatewayDomain 屬性遠端桌面服務
- GatewayDomain 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayDomain 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384166"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a><span data-ttu-id="e9759-106">IMsRdpClientTransportSettings2：： GatewayDomain 屬性</span><span class="sxs-lookup"><span data-stu-id="e9759-106">IMsRdpClientTransportSettings2::GatewayDomain property</span></span>

<span data-ttu-id="e9759-107">指定或抓取提供給遠端桌面閘道 (RD 閘道) 伺服器之使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e9759-107">Specifies or retrieves the domain name of a user that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="e9759-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9759-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9759-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9759-109">Syntax</span></span>


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a><span data-ttu-id="e9759-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e9759-110">Property value</span></span>

<span data-ttu-id="e9759-111">提供用來連接到 RD 閘道伺服器的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e9759-111">The domain name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9759-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e9759-112">Error codes</span></span>

<span data-ttu-id="e9759-113">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e9759-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9759-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9759-114">Requirements</span></span>



| <span data-ttu-id="e9759-115">需求</span><span class="sxs-lookup"><span data-stu-id="e9759-115">Requirement</span></span> | <span data-ttu-id="e9759-116">值</span><span class="sxs-lookup"><span data-stu-id="e9759-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9759-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9759-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e9759-118">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="e9759-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="e9759-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9759-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e9759-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9759-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="e9759-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e9759-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9759-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9759-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e9759-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e9759-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9759-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9759-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e9759-125">IID</span><span class="sxs-lookup"><span data-stu-id="e9759-125">IID</span></span><br/>                      | <span data-ttu-id="e9759-126">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="e9759-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9759-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9759-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9759-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="e9759-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="e9759-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="e9759-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





