---
description: 定義用於資料加密和解密的密碼演算法。
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: 'DOT11_CIPHER_ALGORITHM 列舉 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996800"
---
# <a name="dot11_cipher_algorithm-enumeration"></a><span data-ttu-id="5e620-103">DOT11 \_ 加密 \_ 演算法列舉</span><span class="sxs-lookup"><span data-stu-id="5e620-103">DOT11\_CIPHER\_ALGORITHM enumeration</span></span>

<span data-ttu-id="5e620-104">**DOT11 \_ CIPHER \_ 演算法** 列舉型別會定義用於資料加密和解密的密碼演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-104">The **DOT11\_CIPHER\_ALGORITHM** enumerated type defines a cipher algorithm for data encryption and decryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e620-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e620-105">Syntax</span></span>


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="5e620-106">常數</span><span class="sxs-lookup"><span data-stu-id="5e620-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5e620-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ 加密 \_ ALGO \_ 無**</span><span class="sxs-lookup"><span data-stu-id="5e620-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11\_CIPHER\_ALGO\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-108">指定不啟用或支援任何加密演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-108">Specifies that no cipher algorithm is enabled or supported.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP40**</span><span class="sxs-lookup"><span data-stu-id="5e620-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11\_CIPHER\_ALGO\_WEP40**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-110">指定有線對等隱私權 (WEP) 演算法，這是 802.11-1999 標準中指定的 RC4 型演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-110">Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.</span></span> <span data-ttu-id="5e620-111">此列舉值會以40位加密金鑰指定 WEP 密碼演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-111">This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11 \_ CIPHER \_ ALGO \_ TKIP**</span><span class="sxs-lookup"><span data-stu-id="5e620-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11\_CIPHER\_ALGO\_TKIP**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-113">指定 (TKIP) 演算法的暫時金鑰完整性通訊協定，這是以 RC4 為基礎的加密套件，以 WPA 規格和 IEEE 802.11 i-2004 標準中定義的演算法為基礎。</span><span class="sxs-lookup"><span data-stu-id="5e620-113">Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard.</span></span> <span data-ttu-id="5e620-114">此加密也會使用 Michael 訊息完整性代碼 (MIC) 演算法來進行偽造保護。</span><span class="sxs-lookup"><span data-stu-id="5e620-114">This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ CIPHER \_ ALGO \_ CCMP**</span><span class="sxs-lookup"><span data-stu-id="5e620-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11\_CIPHER\_ALGO\_CCMP**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-116">指定 AES CCMP 演算法，如同 IEEE 802.11 i-2004 標準和 RFC 3610 中所指定。</span><span class="sxs-lookup"><span data-stu-id="5e620-116">Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610.</span></span> <span data-ttu-id="5e620-117">進階加密標準 (AES) 是 FIPS PUB 197 中定義的加密演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-117">Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP104**</span><span class="sxs-lookup"><span data-stu-id="5e620-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11\_CIPHER\_ALGO\_WEP104**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-119">使用104位加密金鑰指定 WEP 密碼演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-119">Specifies a WEP cipher algorithm with a 104-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ WPA \_ USE \_ GROUP**</span><span class="sxs-lookup"><span data-stu-id="5e620-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11\_CIPHER\_ALGO\_WPA\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-121">指定 Wi-Fi 保護的存取 (WPA) 使用群組金鑰加密套件。</span><span class="sxs-lookup"><span data-stu-id="5e620-121">Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite.</span></span> <span data-ttu-id="5e620-122">如需有關使用群組金鑰加密套件的詳細資訊，請參閱 IEEE 802.11 i-2004 標準的 < 子句7.3.2.25.1。</span><span class="sxs-lookup"><span data-stu-id="5e620-122">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ RSN \_ USE \_ GROUP**</span><span class="sxs-lookup"><span data-stu-id="5e620-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11\_CIPHER\_ALGO\_RSN\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-124">指定健全的安全性網路 (RSN) 使用群組金鑰加密套件。</span><span class="sxs-lookup"><span data-stu-id="5e620-124">Specifies a Robust Security Network (RSN) Use Group Key cipher suite.</span></span> <span data-ttu-id="5e620-125">如需有關使用群組金鑰加密套件的詳細資訊，請參閱 IEEE 802.11 i-2004 標準的 < 子句7.3.2.25.1。</span><span class="sxs-lookup"><span data-stu-id="5e620-125">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP**</span><span class="sxs-lookup"><span data-stu-id="5e620-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11\_CIPHER\_ALGO\_WEP**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-127">指定具有任何長度之加密金鑰的 WEP 加密演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-127">Specifies a WEP cipher algorithm with a cipher key of any length.</span></span>

</dd> <dt>

<span data-ttu-id="5e620-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="5e620-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11\_CIPHER\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-129">指定範圍的開頭，此範圍用來定義獨立硬體廠商 (IHV) 所開發的專屬加密演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-129">Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="5e620-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ END**</span><span class="sxs-lookup"><span data-stu-id="5e620-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11\_CIPHER\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="5e620-131">指定範圍的結尾，此範圍用來定義由 IHV 所開發的專屬加密演算法。</span><span class="sxs-lookup"><span data-stu-id="5e620-131">Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e620-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e620-132">Requirements</span></span>



| <span data-ttu-id="5e620-133">需求</span><span class="sxs-lookup"><span data-stu-id="5e620-133">Requirement</span></span> | <span data-ttu-id="5e620-134">值</span><span class="sxs-lookup"><span data-stu-id="5e620-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e620-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e620-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5e620-136">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e620-136">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5e620-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e620-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5e620-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e620-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="5e620-139">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5e620-139">Redistributable</span></span><br/>          | <span data-ttu-id="5e620-140">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="5e620-140">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="5e620-141">標頭</span><span class="sxs-lookup"><span data-stu-id="5e620-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e620-142"><dt>Wlantypes (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="5e620-142"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e620-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e620-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e620-144">**DOT11 \_ AUTH \_ CIPHER \_ 配對**</span><span class="sxs-lookup"><span data-stu-id="5e620-144">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="5e620-145">**可用的 WLAN \_ \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="5e620-145">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="5e620-146">**WLAN \_ 安全性 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="5e620-146">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




