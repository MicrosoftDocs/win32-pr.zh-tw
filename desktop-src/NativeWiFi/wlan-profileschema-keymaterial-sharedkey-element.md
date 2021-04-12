---
description: 包含網路金鑰或複雜密碼。
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: keyMaterial (sharedKey) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192965"
---
# <a name="keymaterial-sharedkey-element"></a><span data-ttu-id="a49a1-103">keyMaterial (sharedKey) 元素</span><span class="sxs-lookup"><span data-stu-id="a49a1-103">keyMaterial (sharedKey) Element</span></span>

<span data-ttu-id="a49a1-104">KeyMaterial (sharedKey) 元素包含網路金鑰或複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="a49a1-104">The keyMaterial (sharedKey) element contains a network key or passphrase.</span></span> <span data-ttu-id="a49a1-105">如果 [**protected**](wlan-profileschema-protected-sharedkey-element.md) 專案的值為 TRUE，則此金鑰材料會加密;否則，就不會加密金鑰內容。</span><span class="sxs-lookup"><span data-stu-id="a49a1-105">If the [**protected**](wlan-profileschema-protected-sharedkey-element.md) element has a value of TRUE, then this key material is encrypted; otherwise, the key material is unencrypted.</span></span> <span data-ttu-id="a49a1-106">加密金鑰內容以十六進位形式表示。</span><span class="sxs-lookup"><span data-stu-id="a49a1-106">Encrypted key material is expressed in hexadecimal form.</span></span>

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

<span data-ttu-id="a49a1-107">元素是由 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="a49a1-107">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a49a1-108">備註</span><span class="sxs-lookup"><span data-stu-id="a49a1-108">Remarks</span></span>

<span data-ttu-id="a49a1-109">KeyMaterial 元素的有效值範圍會依 [**驗證和**](wlan-profileschema-authentication-authencryption-element.md)[**加密**](wlan-profileschema-encryption-authencryption-element.md)元素所指定的驗證和加密類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="a49a1-109">The range of valid values for the keyMaterial element varies by the type of authentication and encryption used, as specified by the [**authentication**](wlan-profileschema-authentication-authencryption-element.md) and [**encryption**](wlan-profileschema-encryption-authencryption-element.md) elements.</span></span> <span data-ttu-id="a49a1-110">它也會因 [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)而異。</span><span class="sxs-lookup"><span data-stu-id="a49a1-110">It also varies by [**keyType**](wlan-profileschema-keytype-sharedkey-element.md).</span></span>

<span data-ttu-id="a49a1-111">下表顯示某些驗證和加密配對的有效 **keyMaterial** 值。</span><span class="sxs-lookup"><span data-stu-id="a49a1-111">The following table shows valid **keyMaterial** values for some authentication and encryption pairs.</span></span>



| <span data-ttu-id="a49a1-112">[**驗證**](wlan-profileschema-authentication-authencryption-element.md) 值</span><span class="sxs-lookup"><span data-stu-id="a49a1-112">[**authentication**](wlan-profileschema-authentication-authencryption-element.md) value</span></span> | <span data-ttu-id="a49a1-113">[**加密**](wlan-profileschema-encryption-authencryption-element.md) 值</span><span class="sxs-lookup"><span data-stu-id="a49a1-113">[**encryption**](wlan-profileschema-encryption-authencryption-element.md) value</span></span> | <span data-ttu-id="a49a1-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) 值</span><span class="sxs-lookup"><span data-stu-id="a49a1-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) value</span></span> | <span data-ttu-id="a49a1-115">有效的 **keyMaterial** 值</span><span class="sxs-lookup"><span data-stu-id="a49a1-115">Valid **keyMaterial** values</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49a1-116">開啟或共用</span><span class="sxs-lookup"><span data-stu-id="a49a1-116">open or shared</span></span>                                                                           | <span data-ttu-id="a49a1-117">WEP</span><span class="sxs-lookup"><span data-stu-id="a49a1-117">WEP</span></span>                                                                              | <span data-ttu-id="a49a1-118">networkKey</span><span class="sxs-lookup"><span data-stu-id="a49a1-118">networkKey</span></span>                                                            | <span data-ttu-id="a49a1-119">此元素包含5或13個 ANSI 字元的 WEP 金鑰，或10或26個十六進位字元。</span><span class="sxs-lookup"><span data-stu-id="a49a1-119">This element contains a WEP key of 5 or 13 ANSI characters, or of 10 or 26 hexadecimal characters.</span></span>                                                                                             |
| <span data-ttu-id="a49a1-120">WPAPSK 或 WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="a49a1-120">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="a49a1-121">TKIP 或 AES</span><span class="sxs-lookup"><span data-stu-id="a49a1-121">TKIP or AES</span></span>                                                                      | <span data-ttu-id="a49a1-122">passPhrase</span><span class="sxs-lookup"><span data-stu-id="a49a1-122">passPhrase</span></span>                                                            | <span data-ttu-id="a49a1-123">此元素包含8到 63 ASCII 字元的複雜密碼，也就是從32到126的8到 63 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="a49a1-123">This element contains a passphrase of 8 to 63 ASCII characters, that is, 8 to 63 ANSI characters in the range of 32 to 126.</span></span> <span data-ttu-id="a49a1-124">索引鍵值必須符合 802.11 i 所指定的需求。</span><span class="sxs-lookup"><span data-stu-id="a49a1-124">Key values must comply with the requirements specified by 802.11i.</span></span> |
| <span data-ttu-id="a49a1-125">WPAPSK 或 WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="a49a1-125">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="a49a1-126">TKIP 或 AES</span><span class="sxs-lookup"><span data-stu-id="a49a1-126">TKIP or AES</span></span>                                                                      | <span data-ttu-id="a49a1-127">networkKey</span><span class="sxs-lookup"><span data-stu-id="a49a1-127">networkKey</span></span>                                                            | <span data-ttu-id="a49a1-128">此元素包含64十六進位字元的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a49a1-128">This element contains a key of 64 hexadecimal characters.</span></span>                                                                                                                                      |



 

<span data-ttu-id="a49a1-129">在上述指定 ANSI 或 ASCII 字元的情況下，可以輸入 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="a49a1-129">Unicode characters may be entered where ANSI or ASCII characters are specified above.</span></span> <span data-ttu-id="a49a1-130">但是，如果提供的 Unicode 字元無法對應至 ANSI 或 ASCII 字元，則會拒絕所提供的金鑰內容。</span><span class="sxs-lookup"><span data-stu-id="a49a1-130">However, if the supplied Unicode characters cannot be mapped to ANSI or ASCII characters, then the supplied key material is rejected.</span></span>

<span data-ttu-id="a49a1-131">[**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)所傳回的金鑰內容一律會加密。</span><span class="sxs-lookup"><span data-stu-id="a49a1-131">Key material returned by [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) is always encrypted.</span></span> <span data-ttu-id="a49a1-132">此外，如果將未加密的金鑰材料傳遞給 [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)，則金鑰內容會在儲存于設定檔存放區之前自動進行加密。</span><span class="sxs-lookup"><span data-stu-id="a49a1-132">Also, if unencrypted key material is passed to [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), the key material is automatically encrypted before it is stored in the profile store.</span></span>

<span data-ttu-id="a49a1-133">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 金鑰內容永遠不會加密。</span><span class="sxs-lookup"><span data-stu-id="a49a1-133">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The key material is never encrypted.</span></span>

<span data-ttu-id="a49a1-134">如果您的進程在 LocalSystem 帳戶內容中執行，則您可以藉由呼叫 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)來解密金鑰內容。</span><span class="sxs-lookup"><span data-stu-id="a49a1-134">If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span>

## <a name="examples"></a><span data-ttu-id="a49a1-135">範例</span><span class="sxs-lookup"><span data-stu-id="a49a1-135">Examples</span></span>

<span data-ttu-id="a49a1-136">若要查看使用 **keyMaterial** 元素的範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)、 [WPA-個人設定檔範例](wpa-personal-profile-sample.md)和 [WPA2 個人設定檔](wpa2-personal-profile-sample.md)範例。</span><span class="sxs-lookup"><span data-stu-id="a49a1-136">To view sample profiles that use the **keyMaterial** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a49a1-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="a49a1-137">Requirements</span></span>



| <span data-ttu-id="a49a1-138">需求</span><span class="sxs-lookup"><span data-stu-id="a49a1-138">Requirement</span></span> | <span data-ttu-id="a49a1-139">值</span><span class="sxs-lookup"><span data-stu-id="a49a1-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a49a1-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a49a1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a49a1-141">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a49a1-141">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a49a1-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a49a1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a49a1-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a49a1-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a49a1-144">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a49a1-144">Redistributable</span></span><br/>          | <span data-ttu-id="a49a1-145">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="a49a1-145">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a49a1-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a49a1-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="a49a1-147">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="a49a1-147">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a49a1-148">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="a49a1-148">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="a49a1-149">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="a49a1-149">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a49a1-150">**sharedKey (安全性)**</span><span class="sxs-lookup"><span data-stu-id="a49a1-150">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
