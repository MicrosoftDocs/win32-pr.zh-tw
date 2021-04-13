---
title: IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookieSize 屬性
description: GatewayEncryptedAuthCookie 屬性的大小（以字元為單位）。
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedAuthCookieSize 屬性遠端桌面服務
- GatewayEncryptedAuthCookieSize 屬性遠端桌面服務，IMsRdpClientTransportSettings3 介面
- IMsRdpClientTransportSettings3 介面遠端桌面服務，GatewayEncryptedAuthCookieSize 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238245cdb9c0164b69434cf61f790b8f81fa3da2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465789"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a><span data-ttu-id="6fd7a-106">IMsRdpClientTransportSettings3：： GatewayEncryptedAuthCookieSize 屬性</span><span class="sxs-lookup"><span data-stu-id="6fd7a-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookieSize property</span></span>

<span data-ttu-id="6fd7a-107">[**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)屬性的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6fd7a-107">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span>

<span data-ttu-id="6fd7a-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6fd7a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd7a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fd7a-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="6fd7a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6fd7a-110">Property value</span></span>

<span data-ttu-id="6fd7a-111">包含新大小值的 **ULONG** 值。</span><span class="sxs-lookup"><span data-stu-id="6fd7a-111">A **ULONG** value that contains the new size value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd7a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fd7a-112">Requirements</span></span>



| <span data-ttu-id="6fd7a-113">需求</span><span class="sxs-lookup"><span data-stu-id="6fd7a-113">Requirement</span></span> | <span data-ttu-id="6fd7a-114">值</span><span class="sxs-lookup"><span data-stu-id="6fd7a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd7a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6fd7a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd7a-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6fd7a-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="6fd7a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6fd7a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd7a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fd7a-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6fd7a-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6fd7a-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="6fd7a-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd7a-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fd7a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6fd7a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd7a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd7a-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd7a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fd7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd7a-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="6fd7a-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





