---
description: 指出是否已啟用聯邦資訊處理標準 (FIPS) 模式。
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: FIPSMode (authEncryption) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690828"
---
# <a name="fipsmode-authencryption-element"></a><span data-ttu-id="2087e-103">FIPSMode (authEncryption) 元素</span><span class="sxs-lookup"><span data-stu-id="2087e-103">FIPSMode (authEncryption) Element</span></span>

<span data-ttu-id="2087e-104">**FIPSMode** (authEncryption) 元素指出是否已啟用聯邦資訊處理標準 (FIPS) 模式。</span><span class="sxs-lookup"><span data-stu-id="2087e-104">The **FIPSMode** (authEncryption) element indicates whether Federal Information Processing Standards (FIPS) mode is enabled.</span></span> <span data-ttu-id="2087e-105">當無線連線以 FIPS 模式運作時，連接的安全性層級會符合 FIPS 140-2 標準。</span><span class="sxs-lookup"><span data-stu-id="2087e-105">When a wireless connection is operating in FIPS mode, the security level of the connection complies with the FIPS 140-2 standard.</span></span> <span data-ttu-id="2087e-106">如需有關 FIPS 的詳細資訊，請參閱 [Fips 首頁](https://www.itl.nist.gov/fipspubs/)。</span><span class="sxs-lookup"><span data-stu-id="2087e-106">For more information about FIPS, see the [FIPS Home Page](https://www.itl.nist.gov/fipspubs/).</span></span>

<span data-ttu-id="2087e-107">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="2087e-107">This element is optional.</span></span> <span data-ttu-id="2087e-108">如果設定檔中未指定此元素，則不會啟用 FIPS 模式。</span><span class="sxs-lookup"><span data-stu-id="2087e-108">If this element is not specified in a profile, then FIPS mode is not enabled.</span></span>

<span data-ttu-id="2087e-109">只有在符合下列條件時， **FIPSMode** 才可以設定為 TRUE：</span><span class="sxs-lookup"><span data-stu-id="2087e-109">**FIPSMode** can be set to TRUE only when the following conditions are met:</span></span>

-   <span data-ttu-id="2087e-110">[**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md)元素的值為 (， `ESS` 也就是連線是) 的基礎結構連接。</span><span class="sxs-lookup"><span data-stu-id="2087e-110">The [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) element has a value of `ESS` (that is, the connection is an infrastructure connection).</span></span>
-   <span data-ttu-id="2087e-111">[**Authentication**](wlan-profileschema-authentication-authencryption-element.md)元素的值為 `WPA2` 或 `WPA2PSK` 。</span><span class="sxs-lookup"><span data-stu-id="2087e-111">The [**authentication**](wlan-profileschema-authentication-authencryption-element.md) element has a value of `WPA2` or `WPA2PSK`.</span></span>
-   <span data-ttu-id="2087e-112">[**加密**](wlan-profileschema-encryption-authencryption-element.md)元素的值為 `AES` 。</span><span class="sxs-lookup"><span data-stu-id="2087e-112">The [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of `AES`.</span></span>

<span data-ttu-id="2087e-113">不同于 WLAN 設定檔架構中的大部分元素 \_ ，此元素位於 `https://www.microsoft.com/networking/WLAN/profile/v2` 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="2087e-113">Unlike most elements in the WLAN\_profile schema, this element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span></span>

<span data-ttu-id="2087e-114">如果無線介面的微型埠驅動程式不支援 FIPS 模式， **FIPSMode** 元素的值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2087e-114">The value of the **FIPSMode** element is ignored if the miniport driver for the wireless interface does not support FIPS mode.</span></span>

<span data-ttu-id="2087e-115">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="2087e-115">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span> <span data-ttu-id="2087e-116">如果設定檔中有 **FIPSMode** ，則會忽略元素。</span><span class="sxs-lookup"><span data-stu-id="2087e-116">If **FIPSMode** is present in a profile, the element is ignored.</span></span>

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

<span data-ttu-id="2087e-117">元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="2087e-117">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2087e-118">備註</span><span class="sxs-lookup"><span data-stu-id="2087e-118">Remarks</span></span>

<span data-ttu-id="2087e-119">您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。</span><span class="sxs-lookup"><span data-stu-id="2087e-119">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="2087e-120">如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="2087e-120">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="examples"></a><span data-ttu-id="2087e-121">範例</span><span class="sxs-lookup"><span data-stu-id="2087e-121">Examples</span></span>

<span data-ttu-id="2087e-122">若要查看使用 **FIPSMode** 元素的範例設定檔，請參閱 [FIPS 設定檔範例](fips-profile-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="2087e-122">To view a sample profile that uses the **FIPSMode** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2087e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2087e-123">Requirements</span></span>



| <span data-ttu-id="2087e-124">需求</span><span class="sxs-lookup"><span data-stu-id="2087e-124">Requirement</span></span> | <span data-ttu-id="2087e-125">值</span><span class="sxs-lookup"><span data-stu-id="2087e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2087e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2087e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2087e-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2087e-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2087e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2087e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2087e-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2087e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2087e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2087e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="2087e-131">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="2087e-131">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2087e-132">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="2087e-132">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="2087e-133">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="2087e-133">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2087e-134">**authEncryption (安全性)**</span><span class="sxs-lookup"><span data-stu-id="2087e-134">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
