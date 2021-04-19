---
description: 指出共用金鑰是否為網路金鑰或密碼片語。
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: keyType (sharedKey) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974704"
---
# <a name="keytype-sharedkey-element"></a><span data-ttu-id="76341-103">keyType (sharedKey) 元素</span><span class="sxs-lookup"><span data-stu-id="76341-103">keyType (sharedKey) Element</span></span>

<span data-ttu-id="76341-104">KeyType (sharedKey) 元素會指出共用金鑰是否為網路金鑰或密碼片語。</span><span class="sxs-lookup"><span data-stu-id="76341-104">The keyType (sharedKey) element indicates whether the shared key will be a network key or a pass phrase.</span></span>

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="76341-105">元素是由 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="76341-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="76341-106">備註</span><span class="sxs-lookup"><span data-stu-id="76341-106">Remarks</span></span>

<span data-ttu-id="76341-107">當 [**加密**](wlan-profileschema-encryption-authencryption-element.md) 元素的值為 WEP 時， **keyType** 必須設為 **networkKey**。</span><span class="sxs-lookup"><span data-stu-id="76341-107">When the [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of WEP, **keyType** must be set to **networkKey**.</span></span>

## <a name="examples"></a><span data-ttu-id="76341-108">範例</span><span class="sxs-lookup"><span data-stu-id="76341-108">Examples</span></span>

<span data-ttu-id="76341-109">若要查看使用 **keyType** 元素的範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)、 [WPA-個人設定檔範例](wpa-personal-profile-sample.md)和 [WPA2 個人設定檔](wpa2-personal-profile-sample.md)範例。</span><span class="sxs-lookup"><span data-stu-id="76341-109">To view sample profiles that use the **keyType** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76341-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="76341-110">Requirements</span></span>



| <span data-ttu-id="76341-111">需求</span><span class="sxs-lookup"><span data-stu-id="76341-111">Requirement</span></span> | <span data-ttu-id="76341-112">值</span><span class="sxs-lookup"><span data-stu-id="76341-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="76341-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76341-113">Minimum supported client</span></span><br/> | <span data-ttu-id="76341-114">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76341-114">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="76341-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76341-115">Minimum supported server</span></span><br/> | <span data-ttu-id="76341-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76341-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="76341-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="76341-117">Redistributable</span></span><br/>          | <span data-ttu-id="76341-118">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="76341-118">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="76341-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76341-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="76341-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="76341-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="76341-121">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="76341-121">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="76341-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="76341-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="76341-123">**sharedKey (安全性)**</span><span class="sxs-lookup"><span data-stu-id="76341-123">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




