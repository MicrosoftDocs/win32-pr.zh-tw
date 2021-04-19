---
title: IMsRdpClientTransportSettings2 GatewayUserName 屬性
description: 指定或抓取提供給遠端桌面閘道 (RD 閘道) server 的使用者名稱。
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- GatewayUserName 屬性遠端桌面服務
- GatewayUserName 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayUserName 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001102"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a><span data-ttu-id="d29b1-106">IMsRdpClientTransportSettings2：： GatewayUserName 屬性</span><span class="sxs-lookup"><span data-stu-id="d29b1-106">IMsRdpClientTransportSettings2::GatewayUserName property</span></span>

<span data-ttu-id="d29b1-107">指定或抓取提供給遠端桌面閘道 (RD 閘道) server 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d29b1-107">Specifies or retrieves the user name that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="d29b1-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d29b1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d29b1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d29b1-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a><span data-ttu-id="d29b1-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="d29b1-110">Property value</span></span>

<span data-ttu-id="d29b1-111">提供用來連接到 RD 閘道伺服器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d29b1-111">The user name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d29b1-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d29b1-112">Error codes</span></span>

<span data-ttu-id="d29b1-113">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="d29b1-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29b1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d29b1-114">Requirements</span></span>



| <span data-ttu-id="d29b1-115">需求</span><span class="sxs-lookup"><span data-stu-id="d29b1-115">Requirement</span></span> | <span data-ttu-id="d29b1-116">值</span><span class="sxs-lookup"><span data-stu-id="d29b1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d29b1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d29b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d29b1-118">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="d29b1-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="d29b1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d29b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d29b1-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d29b1-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="d29b1-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d29b1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d29b1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d29b1-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="d29b1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d29b1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d29b1-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d29b1-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="d29b1-125">IID</span><span class="sxs-lookup"><span data-stu-id="d29b1-125">IID</span></span><br/>                      | <span data-ttu-id="d29b1-126">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="d29b1-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d29b1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d29b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29b1-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="d29b1-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="d29b1-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="d29b1-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





