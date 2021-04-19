---
description: 指定要用於此設定檔的驗證和加密組。
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: authEncryption (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976783"
---
# <a name="authencryption-security-element"></a><span data-ttu-id="8b437-103">authEncryption (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="8b437-103">authEncryption (security) Element</span></span>

<span data-ttu-id="8b437-104">AuthEncryption (security) 元素會指定要用於此設定檔的驗證和加密組。</span><span class="sxs-lookup"><span data-stu-id="8b437-104">The authEncryption (security) element specifies the authentication and encryption pair to be used for this profile.</span></span>

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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

<span data-ttu-id="8b437-105">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="8b437-105">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8b437-106">子元素</span><span class="sxs-lookup"><span data-stu-id="8b437-106">Child elements</span></span>



| <span data-ttu-id="8b437-107">元素</span><span class="sxs-lookup"><span data-stu-id="8b437-107">Element</span></span>                                                                            | <span data-ttu-id="8b437-108">類型</span><span class="sxs-lookup"><span data-stu-id="8b437-108">Type</span></span>                                                              | <span data-ttu-id="8b437-109">Description</span><span class="sxs-lookup"><span data-stu-id="8b437-109">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b437-110">**認證**</span><span class="sxs-lookup"><span data-stu-id="8b437-110">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="8b437-111">指定必須用來連接到無線區域網路的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="8b437-111">Specifies the authentication method that must be used to connect to the wireless LAN.</span></span><br/> |
| [<span data-ttu-id="8b437-112">**加密**</span><span class="sxs-lookup"><span data-stu-id="8b437-112">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="8b437-113">設定用來連接到無線區域網路的資料加密。</span><span class="sxs-lookup"><span data-stu-id="8b437-113">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                       |
| [<span data-ttu-id="8b437-114">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="8b437-114">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="8b437-115">boolean</span><span class="sxs-lookup"><span data-stu-id="8b437-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="8b437-116">指出是否使用 802.1 X。</span><span class="sxs-lookup"><span data-stu-id="8b437-116">Indicates whether 802.1X is used.</span></span><br/>                                                     |



## <a name="remarks"></a><span data-ttu-id="8b437-117">備註</span><span class="sxs-lookup"><span data-stu-id="8b437-117">Remarks</span></span>

<span data-ttu-id="8b437-118">[**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md)元素可以插入做為 **authEncryption** 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="8b437-118">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the **authEncryption** element.</span></span>

## <a name="examples"></a><span data-ttu-id="8b437-119">範例</span><span class="sxs-lookup"><span data-stu-id="8b437-119">Examples</span></span>

<span data-ttu-id="8b437-120">若要查看使用 **authEncryption** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="8b437-120">To view sample profiles that use the **authEncryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span> <span data-ttu-id="8b437-121">若要查看使用 [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) 元素的範例設定檔，請參閱 [FIPS 設定檔範例](fips-profile-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="8b437-121">To view a sample profile that uses the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b437-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b437-122">Requirements</span></span>



| <span data-ttu-id="8b437-123">需求</span><span class="sxs-lookup"><span data-stu-id="8b437-123">Requirement</span></span> | <span data-ttu-id="8b437-124">值</span><span class="sxs-lookup"><span data-stu-id="8b437-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8b437-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b437-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8b437-126">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b437-126">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8b437-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b437-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8b437-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b437-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="8b437-129">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8b437-129">Redistributable</span></span><br/>          | <span data-ttu-id="8b437-130">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="8b437-130">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8b437-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b437-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b437-132">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="8b437-132">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="8b437-133">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="8b437-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8b437-134">**安全**</span><span class="sxs-lookup"><span data-stu-id="8b437-134">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="8b437-135">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="8b437-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8b437-136">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="8b437-136">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
