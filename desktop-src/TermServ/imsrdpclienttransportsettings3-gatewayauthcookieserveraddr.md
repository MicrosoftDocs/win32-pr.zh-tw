---
title: IMsRdpClientTransportSettings3 GatewayAuthCookieServerAddr 屬性
description: 以 cookie 為基礎的驗證的伺服器位址。
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- GatewayAuthCookieServerAddr 屬性遠端桌面服務
- GatewayAuthCookieServerAddr 屬性遠端桌面服務，IMsRdpClientTransportSettings3 介面
- IMsRdpClientTransportSettings3 介面遠端桌面服務，GatewayAuthCookieServerAddr 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc238129d0bb9f698e90fc5e1de85e7257a4d16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466857"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a><span data-ttu-id="f23da-106">IMsRdpClientTransportSettings3：： GatewayAuthCookieServerAddr 屬性</span><span class="sxs-lookup"><span data-stu-id="f23da-106">IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property</span></span>

<span data-ttu-id="f23da-107">以 cookie 為基礎的驗證的伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="f23da-107">The server address for cookie-based authentication.</span></span>

<span data-ttu-id="f23da-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f23da-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23da-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f23da-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="f23da-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="f23da-110">Property value</span></span>

<span data-ttu-id="f23da-111">以 cookie 為基礎的驗證的新伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="f23da-111">The new server address for cookie-based authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23da-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f23da-112">Requirements</span></span>



| <span data-ttu-id="f23da-113">需求</span><span class="sxs-lookup"><span data-stu-id="f23da-113">Requirement</span></span> | <span data-ttu-id="f23da-114">值</span><span class="sxs-lookup"><span data-stu-id="f23da-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f23da-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f23da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f23da-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f23da-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="f23da-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f23da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f23da-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f23da-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f23da-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f23da-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="f23da-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f23da-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f23da-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f23da-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f23da-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f23da-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23da-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f23da-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23da-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="f23da-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





