---
title: IMsRdpClientTransportSettings2 GatewayEncryptedOtpCookieSize 屬性
description: 指定或抓取加密的一次性密碼 (OTP) cookie 的大小。
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedOtpCookieSize 屬性遠端桌面服務
- GatewayEncryptedOtpCookieSize 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayEncryptedOtpCookieSize 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e714b7c03e898b29b1ae02e3b19d65fde8dfcb91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685867"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a><span data-ttu-id="5ada2-106">IMsRdpClientTransportSettings2：： GatewayEncryptedOtpCookieSize 屬性</span><span class="sxs-lookup"><span data-stu-id="5ada2-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize property</span></span>

<span data-ttu-id="5ada2-107">指定或抓取加密的一次性密碼 (OTP) cookie 的大小。</span><span class="sxs-lookup"><span data-stu-id="5ada2-107">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="5ada2-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ada2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ada2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ada2-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="5ada2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5ada2-110">Property value</span></span>

<span data-ttu-id="5ada2-111">指定或抓取加密的一次性密碼 (OTP) cookie 的大小。</span><span class="sxs-lookup"><span data-stu-id="5ada2-111">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ada2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ada2-112">Requirements</span></span>



| <span data-ttu-id="5ada2-113">需求</span><span class="sxs-lookup"><span data-stu-id="5ada2-113">Requirement</span></span> | <span data-ttu-id="5ada2-114">值</span><span class="sxs-lookup"><span data-stu-id="5ada2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ada2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ada2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5ada2-116">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="5ada2-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="5ada2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ada2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5ada2-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ada2-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="5ada2-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5ada2-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ada2-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ada2-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5ada2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5ada2-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ada2-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ada2-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5ada2-123">IID</span><span class="sxs-lookup"><span data-stu-id="5ada2-123">IID</span></span><br/>                      | <span data-ttu-id="5ada2-124">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="5ada2-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ada2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ada2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ada2-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="5ada2-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="5ada2-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="5ada2-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





