---
title: IMsRdpClientTransportSettings3 GatewayCredSourceCookie 屬性
description: 指定認證來源是否以 cookie 為基礎。
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- GatewayCredSourceCookie 屬性遠端桌面服務
- GatewayCredSourceCookie 屬性遠端桌面服務，IMsRdpClientTransportSettings3 介面
- IMsRdpClientTransportSettings3 介面遠端桌面服務，GatewayCredSourceCookie 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968996"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a><span data-ttu-id="1dfd5-106">IMsRdpClientTransportSettings3：： GatewayCredSourceCookie 屬性</span><span class="sxs-lookup"><span data-stu-id="1dfd5-106">IMsRdpClientTransportSettings3::GatewayCredSourceCookie property</span></span>

<span data-ttu-id="1dfd5-107">指定認證來源是否以 cookie 為基礎。</span><span class="sxs-lookup"><span data-stu-id="1dfd5-107">Specifies if the credential source is cookie based.</span></span> <span data-ttu-id="1dfd5-108">如果認證來源是以 cookie 為基礎或為零，則會包含一個。</span><span class="sxs-lookup"><span data-stu-id="1dfd5-108">Contains one if the credential source is cookie-based or zero otherwise.</span></span>

<span data-ttu-id="1dfd5-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1dfd5-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfd5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dfd5-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a><span data-ttu-id="1dfd5-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="1dfd5-111">Property value</span></span>

<span data-ttu-id="1dfd5-112">**ULONG** 值，指定認證來源是否以 cookie 為基礎。</span><span class="sxs-lookup"><span data-stu-id="1dfd5-112">A **ULONG** value that specifies if the credential source is cookie based.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfd5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dfd5-113">Requirements</span></span>



| <span data-ttu-id="1dfd5-114">需求</span><span class="sxs-lookup"><span data-stu-id="1dfd5-114">Requirement</span></span> | <span data-ttu-id="1dfd5-115">值</span><span class="sxs-lookup"><span data-stu-id="1dfd5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfd5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1dfd5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfd5-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1dfd5-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="1dfd5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1dfd5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfd5-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dfd5-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1dfd5-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1dfd5-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="1dfd5-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dfd5-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1dfd5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1dfd5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dfd5-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dfd5-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfd5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1dfd5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfd5-125">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="1dfd5-125">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





