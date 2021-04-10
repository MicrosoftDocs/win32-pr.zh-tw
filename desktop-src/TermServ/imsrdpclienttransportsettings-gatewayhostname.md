---
title: IMsRdpClientTransportSettings GatewayHostname 屬性
description: 指定遠端桌面閘道 (RD 閘道) server 的主機名稱。
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- GatewayHostname 屬性遠端桌面服務
- GatewayHostname 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayHostname 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317155"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a><span data-ttu-id="bd046-106">IMsRdpClientTransportSettings：： GatewayHostname 屬性</span><span class="sxs-lookup"><span data-stu-id="bd046-106">IMsRdpClientTransportSettings::GatewayHostname property</span></span>

<span data-ttu-id="bd046-107">指定遠端桌面閘道 (RD 閘道) server 的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="bd046-107">Specifies the host name of the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="bd046-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd046-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd046-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd046-109">Syntax</span></span>


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a><span data-ttu-id="bd046-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bd046-110">Property value</span></span>

<span data-ttu-id="bd046-111">包含 RD 閘道 server 主機名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="bd046-111">A string that contains the RD Gateway server host name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd046-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bd046-112">Error codes</span></span>

<span data-ttu-id="bd046-113">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="bd046-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd046-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd046-114">Requirements</span></span>



| <span data-ttu-id="bd046-115">需求</span><span class="sxs-lookup"><span data-stu-id="bd046-115">Requirement</span></span> | <span data-ttu-id="bd046-116">值</span><span class="sxs-lookup"><span data-stu-id="bd046-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd046-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd046-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd046-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd046-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bd046-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd046-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd046-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd046-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bd046-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bd046-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd046-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd046-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd046-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bd046-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd046-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd046-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd046-125">IID</span><span class="sxs-lookup"><span data-stu-id="bd046-125">IID</span></span><br/>                      | <span data-ttu-id="bd046-126">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="bd046-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd046-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd046-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd046-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="bd046-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





