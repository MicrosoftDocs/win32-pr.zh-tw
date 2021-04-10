---
description: 密碼編譯通訊協定的預先定義常數。 這些值定義于 Wincrypt 中。
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: '通訊協定旗標 (Wincrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944869"
---
# <a name="protocol-flags"></a><span data-ttu-id="7e495-104">通訊協定旗標</span><span class="sxs-lookup"><span data-stu-id="7e495-104">Protocol Flags</span></span>

<span data-ttu-id="7e495-105">以下是密碼編譯通訊協定的預先定義常數。</span><span class="sxs-lookup"><span data-stu-id="7e495-105">The following are predefined constants for cryptography protocols.</span></span> <span data-ttu-id="7e495-106">這些值定義于 Wincrypt 中。</span><span class="sxs-lookup"><span data-stu-id="7e495-106">These values are defined in Wincrypt.h.</span></span>



| <span data-ttu-id="7e495-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="7e495-107">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="7e495-108">Description</span><span class="sxs-lookup"><span data-stu-id="7e495-108">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <span data-ttu-id="7e495-109"><dt>**CRYPT \_旗標 \_ IPSEC**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="7e495-109"><dt>**CRYPT\_FLAG\_IPSEC**</dt> <dt>0x0010</dt></span></span> </dl>       | <span data-ttu-id="7e495-110">網際網路通訊協定安全性 (IPsec) 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7e495-110">Internet protocol security (IPsec) protocol.</span></span><br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <span data-ttu-id="7e495-111"><dt>**CRYPT \_旗標 \_ PCT1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="7e495-111"><dt>**CRYPT\_FLAG\_PCT1**</dt> <dt>0x0001</dt></span></span> </dl>          | <span data-ttu-id="7e495-112">私人通訊傳輸 (PCT) 第1版通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7e495-112">Private communications transport (PCT) version 1 protocol.</span></span><br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <span data-ttu-id="7e495-113"><dt>**CRYPT \_旗標 \_ 簽署**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="7e495-113"><dt>**CRYPT\_FLAG\_SIGNING**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="7e495-114">簽署通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7e495-114">Signing protocol.</span></span><br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <span data-ttu-id="7e495-115"><dt>**CRYPT \_旗標 \_ SSL2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="7e495-115"><dt>**CRYPT\_FLAG\_SSL2**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="7e495-116">安全通訊端層 (SSL) 第2版通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7e495-116">Secure sockets layer (SSL) version 2 protocol.</span></span><br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <span data-ttu-id="7e495-117"><dt>**CRYPT \_旗標 \_ SSL3**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="7e495-117"><dt>**CRYPT\_FLAG\_SSL3**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="7e495-118">SSL 第3版通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7e495-118">SSL version 3 protocol.</span></span><br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <span data-ttu-id="7e495-119"><dt>**CRYPT \_旗標 \_ TLS1**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="7e495-119"><dt>**CRYPT\_FLAG\_TLS1**</dt> <dt>0x0008</dt></span></span> </dl>          | <span data-ttu-id="7e495-120">傳輸層安全性 (TLS) 第1版通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7e495-120">Transport layer security (TLS) version 1 protocol.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="7e495-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e495-121">Requirements</span></span>



| <span data-ttu-id="7e495-122">需求</span><span class="sxs-lookup"><span data-stu-id="7e495-122">Requirement</span></span> | <span data-ttu-id="7e495-123">值</span><span class="sxs-lookup"><span data-stu-id="7e495-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e495-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e495-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7e495-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e495-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7e495-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e495-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7e495-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e495-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e495-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7e495-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e495-129"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e495-129"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e495-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e495-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e495-131">**>PROV \_ ENUMALGS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="7e495-131">**PROV\_ENUMALGS\_EX**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




