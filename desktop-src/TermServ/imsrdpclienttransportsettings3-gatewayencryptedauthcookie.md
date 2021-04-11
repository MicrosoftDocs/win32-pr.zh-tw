---
title: IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookie 屬性
description: 加密的驗證 cookie。
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedAuthCookie 屬性遠端桌面服務
- GatewayEncryptedAuthCookie 屬性遠端桌面服務，IMsRdpClientTransportSettings3 介面
- IMsRdpClientTransportSettings3 介面遠端桌面服務，GatewayEncryptedAuthCookie 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317251"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a><span data-ttu-id="140fa-106">IMsRdpClientTransportSettings3：： GatewayEncryptedAuthCookie 屬性</span><span class="sxs-lookup"><span data-stu-id="140fa-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie property</span></span>

<span data-ttu-id="140fa-107">加密的驗證 cookie。</span><span class="sxs-lookup"><span data-stu-id="140fa-107">The encrypted authentication cookie.</span></span> <span data-ttu-id="140fa-108">屬性的大小是由 [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="140fa-108">The size of the property is specified by the [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) property.</span></span>

<span data-ttu-id="140fa-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="140fa-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="140fa-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="140fa-110">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a><span data-ttu-id="140fa-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="140fa-111">Property value</span></span>

<span data-ttu-id="140fa-112">新的加密驗證 cookie。</span><span class="sxs-lookup"><span data-stu-id="140fa-112">The new encrypted authentication cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="140fa-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="140fa-113">Requirements</span></span>



| <span data-ttu-id="140fa-114">需求</span><span class="sxs-lookup"><span data-stu-id="140fa-114">Requirement</span></span> | <span data-ttu-id="140fa-115">值</span><span class="sxs-lookup"><span data-stu-id="140fa-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="140fa-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="140fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="140fa-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="140fa-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="140fa-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="140fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="140fa-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="140fa-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="140fa-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="140fa-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="140fa-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140fa-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="140fa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="140fa-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="140fa-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140fa-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140fa-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="140fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140fa-125">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="140fa-125">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[<span data-ttu-id="140fa-126">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="140fa-126">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





