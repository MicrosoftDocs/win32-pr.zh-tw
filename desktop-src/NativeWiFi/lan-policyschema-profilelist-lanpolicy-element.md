---
description: profileList (LANPolicy) 元素-包含要在網域或電腦層級套用的配置檔案清單。
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: profileList (LANPolicy) 元素
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
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090776"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="bb8a0-103">profileList (LANPolicy) 元素</span><span class="sxs-lookup"><span data-stu-id="bb8a0-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="bb8a0-104">ProfileList (LANPolicy) 元素包含要在網域或電腦層級套用的配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="bb8a0-105">設定檔必須以 [LAN \_ 設定檔架構](lan-profileschema-schema.md)為基礎，並以 [**LANProfile**](lan-profileschema-lanprofile-element.md)的根項目為基礎。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="bb8a0-106">將會忽略以任何其他架構為基礎的設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="bb8a0-107">當 [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) 設定為 FALSE 時，此元素不能出現在 LAN 原則設定檔中。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="bb8a0-108">當 **enableAutoConfig** 設定為 TRUE 時，則需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

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

<span data-ttu-id="bb8a0-109">**ProfileList** 元素是由 [**LANPolicy**](lan-policyschema-lanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb8a0-110">備註</span><span class="sxs-lookup"><span data-stu-id="bb8a0-110">Remarks</span></span>

<span data-ttu-id="bb8a0-111">此元素只可包含一個網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="bb8a0-112">如果在原則中指定一個以上的設定檔，則只會套用第一個網路。</span><span class="sxs-lookup"><span data-stu-id="bb8a0-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb8a0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb8a0-113">Requirements</span></span>



| <span data-ttu-id="bb8a0-114">需求</span><span class="sxs-lookup"><span data-stu-id="bb8a0-114">Requirement</span></span> | <span data-ttu-id="bb8a0-115">值</span><span class="sxs-lookup"><span data-stu-id="bb8a0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb8a0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb8a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb8a0-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb8a0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb8a0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb8a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb8a0-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb8a0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb8a0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb8a0-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb8a0-121">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="bb8a0-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bb8a0-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="bb8a0-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="bb8a0-123">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="bb8a0-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bb8a0-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="bb8a0-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




