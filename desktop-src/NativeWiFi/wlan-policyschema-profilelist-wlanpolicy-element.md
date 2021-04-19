---
description: 包含要在網域或電腦層級套用的配置檔案清單。
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: profileList (WLANPolicy) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980487"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="e181d-103">profileList (WLANPolicy) 元素</span><span class="sxs-lookup"><span data-stu-id="e181d-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="e181d-104">ProfileList (WLANPolicy) 元素包含要在網域或電腦層級套用的配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="e181d-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="e181d-105">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="e181d-105">This element is optional.</span></span> <span data-ttu-id="e181d-106">如果這個元素存在，它必須包含至少一個設定檔。</span><span class="sxs-lookup"><span data-stu-id="e181d-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="e181d-107">設定檔應該以 [WLAN \_ 設定檔架構](wlan-profileschema-schema.md)為基礎，其根項目為 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)。</span><span class="sxs-lookup"><span data-stu-id="e181d-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="e181d-108">**ProfileList** 元素是由 [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="e181d-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e181d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="e181d-109">Requirements</span></span>



| <span data-ttu-id="e181d-110">需求</span><span class="sxs-lookup"><span data-stu-id="e181d-110">Requirement</span></span> | <span data-ttu-id="e181d-111">值</span><span class="sxs-lookup"><span data-stu-id="e181d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e181d-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e181d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e181d-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e181d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e181d-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e181d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e181d-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e181d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e181d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e181d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="e181d-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e181d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e181d-118">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="e181d-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="e181d-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e181d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e181d-120">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="e181d-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




