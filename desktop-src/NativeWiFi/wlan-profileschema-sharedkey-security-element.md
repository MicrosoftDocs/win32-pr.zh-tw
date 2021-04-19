---
description: 包含共用金鑰資訊。
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: sharedKey (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992050"
---
# <a name="sharedkey-security-element"></a><span data-ttu-id="66eba-103">sharedKey (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="66eba-103">sharedKey (security) Element</span></span>

<span data-ttu-id="66eba-104">SharedKey (security) 元素包含共用金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="66eba-104">The sharedKey (security) element contains shared key information.</span></span> <span data-ttu-id="66eba-105">只有在驗證和加密配對需要 WEP 或 PSK 金鑰時，才需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="66eba-105">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span>

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="66eba-106">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="66eba-106">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="66eba-107">子元素</span><span class="sxs-lookup"><span data-stu-id="66eba-107">Child elements</span></span>



| <span data-ttu-id="66eba-108">元素</span><span class="sxs-lookup"><span data-stu-id="66eba-108">Element</span></span>                                                                 | <span data-ttu-id="66eba-109">類型</span><span class="sxs-lookup"><span data-stu-id="66eba-109">Type</span></span>                                                              | <span data-ttu-id="66eba-110">Description</span><span class="sxs-lookup"><span data-stu-id="66eba-110">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66eba-111">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="66eba-111">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md) | [<span data-ttu-id="66eba-112">string</span><span class="sxs-lookup"><span data-stu-id="66eba-112">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="66eba-113">包含網路金鑰或複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="66eba-113">Contains the network key or passphrase.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="66eba-114">**keyType**</span><span class="sxs-lookup"><span data-stu-id="66eba-114">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | <span data-ttu-id="66eba-115">索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="66eba-115">Type of key.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="66eba-116">**受保護**</span><span class="sxs-lookup"><span data-stu-id="66eba-116">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)     | [<span data-ttu-id="66eba-117">boolean</span><span class="sxs-lookup"><span data-stu-id="66eba-117">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="66eba-118">指出金鑰是否已加密。</span><span class="sxs-lookup"><span data-stu-id="66eba-118">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="66eba-119">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 這個元素的值必須為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="66eba-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="66eba-120">備註</span><span class="sxs-lookup"><span data-stu-id="66eba-120">Remarks</span></span>

<span data-ttu-id="66eba-121">若為 Windows Vista 和 Windows Server 2008，與 **sharedKey** 元素相關聯的資料會在儲存至設定檔存放區之前加密。</span><span class="sxs-lookup"><span data-stu-id="66eba-121">For Windows Vista and Windows Server 2008, the data associated with the **sharedKey** element is encrypted before it is saved in the profile store.</span></span>

<span data-ttu-id="66eba-122">若為 windows XP （含 SP3）和 Windows XP （含 SP2）的無線區域網路 API，則不會加密資料。</span><span class="sxs-lookup"><span data-stu-id="66eba-122">For Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, the data is not encrypted.</span></span>

## <a name="examples"></a><span data-ttu-id="66eba-123">範例</span><span class="sxs-lookup"><span data-stu-id="66eba-123">Examples</span></span>

<span data-ttu-id="66eba-124">若要查看使用 **sharedKey** 元素的範例設定檔，請參閱 [非廣播設定檔範例](non-broadcast-profile-sample.md)、 [WPA-個人設定檔範例](wpa-personal-profile-sample.md)和 [WPA2 個人設定檔](wpa2-personal-profile-sample.md)範例。</span><span class="sxs-lookup"><span data-stu-id="66eba-124">To view sample profiles that use the **sharedKey** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66eba-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="66eba-125">Requirements</span></span>



| <span data-ttu-id="66eba-126">需求</span><span class="sxs-lookup"><span data-stu-id="66eba-126">Requirement</span></span> | <span data-ttu-id="66eba-127">值</span><span class="sxs-lookup"><span data-stu-id="66eba-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="66eba-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66eba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66eba-129">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66eba-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="66eba-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66eba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66eba-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66eba-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="66eba-132">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="66eba-132">Redistributable</span></span><br/>          | <span data-ttu-id="66eba-133">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="66eba-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="66eba-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66eba-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="66eba-135">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="66eba-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="66eba-136">**安全**</span><span class="sxs-lookup"><span data-stu-id="66eba-136">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="66eba-137">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="66eba-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="66eba-138">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="66eba-138">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
