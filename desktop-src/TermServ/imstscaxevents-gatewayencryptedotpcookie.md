---
title: IMsRdpClientTransportSettings2 GatewayEncryptedOtpCookie 屬性
description: 指定或抓取加密的一次性密碼 (OTP) cookie。
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedOtpCookie 屬性遠端桌面服務
- GatewayEncryptedOtpCookie 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayEncryptedOtpCookie 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509468"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a><span data-ttu-id="57ed9-106">IMsRdpClientTransportSettings2：： GatewayEncryptedOtpCookie 屬性</span><span class="sxs-lookup"><span data-stu-id="57ed9-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie property</span></span>

<span data-ttu-id="57ed9-107">指定或抓取加密的一次性密碼 (OTP) cookie。</span><span class="sxs-lookup"><span data-stu-id="57ed9-107">Specifies or retrieves the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="57ed9-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="57ed9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ed9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="57ed9-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a><span data-ttu-id="57ed9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="57ed9-110">Property value</span></span>

<span data-ttu-id="57ed9-111">指定或抓取加密的 OTP cookie。</span><span class="sxs-lookup"><span data-stu-id="57ed9-111">Specifies or retrieves the encrypted OTP cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ed9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="57ed9-112">Requirements</span></span>



| <span data-ttu-id="57ed9-113">需求</span><span class="sxs-lookup"><span data-stu-id="57ed9-113">Requirement</span></span> | <span data-ttu-id="57ed9-114">值</span><span class="sxs-lookup"><span data-stu-id="57ed9-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ed9-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57ed9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="57ed9-116">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="57ed9-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="57ed9-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57ed9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="57ed9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57ed9-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="57ed9-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="57ed9-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="57ed9-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ed9-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="57ed9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="57ed9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57ed9-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ed9-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="57ed9-123">IID</span><span class="sxs-lookup"><span data-stu-id="57ed9-123">IID</span></span><br/>                      | <span data-ttu-id="57ed9-124">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="57ed9-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57ed9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57ed9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ed9-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="57ed9-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="57ed9-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="57ed9-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





