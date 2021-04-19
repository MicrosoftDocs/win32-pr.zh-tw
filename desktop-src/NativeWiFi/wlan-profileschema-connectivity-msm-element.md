---
description: 包含各種連接設定。
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: " (.MSM) 元素的連接"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 938e5b19ffab490066fbbe299bd250191d9226a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989062"
---
# <a name="connectivity-msm-element"></a><span data-ttu-id="51bae-103"> (.MSM) 元素的連接</span><span class="sxs-lookup"><span data-stu-id="51bae-103">connectivity (MSM) Element</span></span>

<span data-ttu-id="51bae-104"> (.MSM) 元素的連線，包含各種連線設定。</span><span class="sxs-lookup"><span data-stu-id="51bae-104">The connectivity (MSM) element contains various connectivity settings.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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

<span data-ttu-id="51bae-105">元素是由 [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) 元素定義。</span><span class="sxs-lookup"><span data-stu-id="51bae-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="51bae-106">子元素</span><span class="sxs-lookup"><span data-stu-id="51bae-106">Child elements</span></span>



| <span data-ttu-id="51bae-107">元素</span><span class="sxs-lookup"><span data-stu-id="51bae-107">Element</span></span>                                                            | <span data-ttu-id="51bae-108">類型</span><span class="sxs-lookup"><span data-stu-id="51bae-108">Type</span></span> |
|--------------------------------------------------------------------|------|
| [<span data-ttu-id="51bae-109">**phyType**</span><span class="sxs-lookup"><span data-stu-id="51bae-109">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a><span data-ttu-id="51bae-110">範例</span><span class="sxs-lookup"><span data-stu-id="51bae-110">Examples</span></span>

<span data-ttu-id="51bae-111">若要查看使用 **連接** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="51bae-111">To view sample profiles that use the **connectivity** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51bae-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="51bae-112">Requirements</span></span>



| <span data-ttu-id="51bae-113">需求</span><span class="sxs-lookup"><span data-stu-id="51bae-113">Requirement</span></span> | <span data-ttu-id="51bae-114">值</span><span class="sxs-lookup"><span data-stu-id="51bae-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="51bae-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51bae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="51bae-116">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51bae-116">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51bae-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51bae-117">Minimum supported server</span></span><br/> | <span data-ttu-id="51bae-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51bae-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="51bae-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="51bae-119">Redistributable</span></span><br/>          | <span data-ttu-id="51bae-120">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="51bae-120">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="51bae-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51bae-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="51bae-122">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="51bae-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="51bae-123">**MSM**</span><span class="sxs-lookup"><span data-stu-id="51bae-123">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="51bae-124">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="51bae-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="51bae-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="51bae-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




