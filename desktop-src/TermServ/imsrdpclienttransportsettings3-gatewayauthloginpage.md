---
title: IMsRdpClientTransportSettings3 GatewayAuthLoginPage 屬性
description: 用來驗證使用者的登入網頁位址。
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- GatewayAuthLoginPage 屬性遠端桌面服務
- GatewayAuthLoginPage 屬性遠端桌面服務，IMsRdpClientTransportSettings3 介面
- IMsRdpClientTransportSettings3 介面遠端桌面服務，GatewayAuthLoginPage 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106091"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a><span data-ttu-id="455e3-106">IMsRdpClientTransportSettings3：： GatewayAuthLoginPage 屬性</span><span class="sxs-lookup"><span data-stu-id="455e3-106">IMsRdpClientTransportSettings3::GatewayAuthLoginPage property</span></span>

<span data-ttu-id="455e3-107">用來驗證使用者的登入網頁位址。</span><span class="sxs-lookup"><span data-stu-id="455e3-107">The address of the login webpage to use to authenticate a user.</span></span>

<span data-ttu-id="455e3-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="455e3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="455e3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="455e3-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a><span data-ttu-id="455e3-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="455e3-110">Property value</span></span>

<span data-ttu-id="455e3-111">新的登入網頁位址。</span><span class="sxs-lookup"><span data-stu-id="455e3-111">The new login webpage address.</span></span>

## <a name="requirements"></a><span data-ttu-id="455e3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="455e3-112">Requirements</span></span>



| <span data-ttu-id="455e3-113">需求</span><span class="sxs-lookup"><span data-stu-id="455e3-113">Requirement</span></span> | <span data-ttu-id="455e3-114">值</span><span class="sxs-lookup"><span data-stu-id="455e3-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="455e3-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="455e3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="455e3-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="455e3-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="455e3-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="455e3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="455e3-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="455e3-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="455e3-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="455e3-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="455e3-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="455e3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="455e3-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="455e3-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="455e3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="455e3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455e3-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="455e3-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





