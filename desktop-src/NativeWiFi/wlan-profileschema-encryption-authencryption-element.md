---
description: 指定要用來連接到無線區域網路的資料加密類型。
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: " (authEncryption) 元素加密"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113613"
---
# <a name="encryption-authencryption-element"></a><span data-ttu-id="b2b5a-103"> (authEncryption) 元素加密</span><span class="sxs-lookup"><span data-stu-id="b2b5a-103">encryption (authEncryption) Element</span></span>

<span data-ttu-id="b2b5a-104">Encryption (authEncryption) 元素會指定要用來連線到無線區域網路的資料加密類型。</span><span class="sxs-lookup"><span data-stu-id="b2b5a-104">The encryption (authEncryption) element specifies the type of data encryption to use to connect to a wireless LAN.</span></span>

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b2b5a-105">元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="b2b5a-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b5a-106">備註</span><span class="sxs-lookup"><span data-stu-id="b2b5a-106">Remarks</span></span>

<span data-ttu-id="b2b5a-107">當 **加密** 元素的值為 WEP 時， [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) 必須設為 **networkKey**。</span><span class="sxs-lookup"><span data-stu-id="b2b5a-107">When the **encryption** element has a value of WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) must be set to **networkKey**.</span></span>

<span data-ttu-id="b2b5a-108">AES 加密方法如 [802.1 x](https://ieeexplore.ieee.org/document/1438730) 和 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格中所指定。</span><span class="sxs-lookup"><span data-stu-id="b2b5a-108">The AES encryption method is as specified in the [802.1X](https://ieeexplore.ieee.org/document/1438730) and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="b2b5a-109">範例</span><span class="sxs-lookup"><span data-stu-id="b2b5a-109">Examples</span></span>

<span data-ttu-id="b2b5a-110">若要查看使用 **加密** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="b2b5a-110">To view sample profiles that use the **encryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b5a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2b5a-111">Requirements</span></span>



| <span data-ttu-id="b2b5a-112">需求</span><span class="sxs-lookup"><span data-stu-id="b2b5a-112">Requirement</span></span> | <span data-ttu-id="b2b5a-113">值</span><span class="sxs-lookup"><span data-stu-id="b2b5a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b2b5a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2b5a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b5a-115">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2b5a-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b2b5a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2b5a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b5a-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2b5a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b2b5a-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b2b5a-118">Redistributable</span></span><br/>          | <span data-ttu-id="b2b5a-119">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="b2b5a-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b2b5a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2b5a-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2b5a-121">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b2b5a-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b2b5a-122">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="b2b5a-122">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="b2b5a-123">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b2b5a-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b2b5a-124">**authEncryption (安全性)**</span><span class="sxs-lookup"><span data-stu-id="b2b5a-124">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




