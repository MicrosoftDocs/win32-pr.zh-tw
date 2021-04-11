---
description: 包含無線區域網路原則。
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: WLANPolicy 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114317"
---
# <a name="wlanpolicy-element"></a><span data-ttu-id="3f6d2-103">WLANPolicy 元素</span><span class="sxs-lookup"><span data-stu-id="3f6d2-103">WLANPolicy Element</span></span>

<span data-ttu-id="3f6d2-104">**WLANPolicy** 元素包含無線區域網路原則。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-104">The **WLANPolicy** element contains a wireless LAN policy.</span></span> <span data-ttu-id="3f6d2-105">此元素是無線原則設定檔的唯一根項目。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-105">This element is the unique root element for a wireless policy profile.</span></span>

<span data-ttu-id="3f6d2-106">**WLANPolicy** 元素的目標命名空間為 `https://www.microsoft.com/networking/WLAN/policy/v1` 。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-106">The target namespace for the **WLANPolicy** element is `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
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
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
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
            <xs:element name="profileList"
                minOccurs="0"
            >
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

## <a name="child-elements"></a><span data-ttu-id="3f6d2-107">子元素</span><span class="sxs-lookup"><span data-stu-id="3f6d2-107">Child elements</span></span>



| <span data-ttu-id="3f6d2-108">元素</span><span class="sxs-lookup"><span data-stu-id="3f6d2-108">Element</span></span>                                                                                                                    | <span data-ttu-id="3f6d2-109">類型</span><span class="sxs-lookup"><span data-stu-id="3f6d2-109">Type</span></span>                                                                     | <span data-ttu-id="3f6d2-110">Description</span><span class="sxs-lookup"><span data-stu-id="3f6d2-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f6d2-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="3f6d2-112">boolean</span><span class="sxs-lookup"><span data-stu-id="3f6d2-112">boolean</span></span>                                                                  | <span data-ttu-id="3f6d2-113">指定任何使用者是否可以建立所有使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="3f6d2-114">**允許清單**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-114">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="3f6d2-115">必須允許任何電腦連接的無線區域網路網路清單。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-115">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/>                                       |
| [<span data-ttu-id="3f6d2-116">**封鎖清單**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="3f6d2-117">電腦不能連線的無線區域網路網路清單。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-117">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>                                                    |
| [<span data-ttu-id="3f6d2-118">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-118">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | <span data-ttu-id="3f6d2-119">boolean</span><span class="sxs-lookup"><span data-stu-id="3f6d2-119">boolean</span></span>                                                                  | <span data-ttu-id="3f6d2-120">指定是否封鎖對所有基礎結構網路的存取。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-120">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                                                           |
| [<span data-ttu-id="3f6d2-121">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-121">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | <span data-ttu-id="3f6d2-122">boolean</span><span class="sxs-lookup"><span data-stu-id="3f6d2-122">boolean</span></span>                                                                  | <span data-ttu-id="3f6d2-123">指定是否封鎖對所有特定網路的存取。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-123">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                                                                   |
| [<span data-ttu-id="3f6d2-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-124">**description**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [<span data-ttu-id="3f6d2-125">**nameType**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-125">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="3f6d2-126">無線區域網路原則的描述。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-126">The description of a wireless LAN policy.</span></span> <br/>                                                                                |
| [<span data-ttu-id="3f6d2-127">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-127">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="3f6d2-128">boolean</span><span class="sxs-lookup"><span data-stu-id="3f6d2-128">boolean</span></span>                                                                  | <span data-ttu-id="3f6d2-129">指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-129">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="3f6d2-130">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-130">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="3f6d2-131">包含自動設定模組的全域設定 (配置) 。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-131">Contains the global settings for the Auto Configuration Module (ACM).</span></span> <br/>                                                    |
| [<span data-ttu-id="3f6d2-132">**名字**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-132">**name**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [<span data-ttu-id="3f6d2-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-133">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="3f6d2-134">無線區域網路原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-134">The name of a wireless LAN policy.</span></span> <br/>                                                                                       |
| [<span data-ttu-id="3f6d2-135">**network**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-135">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)                                                             | [<span data-ttu-id="3f6d2-136">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-136">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="3f6d2-137">允許的網路。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-137">An allowed network.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="3f6d2-138">**network**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-138">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)                                                             | [<span data-ttu-id="3f6d2-139">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-139">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="3f6d2-140">封鎖的網路。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-140">A blocked network.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="3f6d2-141">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-141">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | <span data-ttu-id="3f6d2-142">允許和拒絕的網路清單。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-142">The list of allowed and denied networks.</span></span><br/>                                                                                  |
| [<span data-ttu-id="3f6d2-143">**profileList**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-143">**profileList**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="3f6d2-144">包含要在網域或電腦層級套用的配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-144">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                |
| [<span data-ttu-id="3f6d2-145">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="3f6d2-145">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="3f6d2-146">boolean</span><span class="sxs-lookup"><span data-stu-id="3f6d2-146">boolean</span></span>                                                                  | <span data-ttu-id="3f6d2-147">指定已拒絕的網路是否出現在 [ **連接到網路** ] 嚮導中。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-147">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="remarks"></a><span data-ttu-id="3f6d2-148">備註</span><span class="sxs-lookup"><span data-stu-id="3f6d2-148">Remarks</span></span>

<span data-ttu-id="3f6d2-149">若要查看類似樹狀結構中子專案的清單，請參閱 [WLAN \_ 原則架構元素](wlan-policyschema-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="3f6d2-149">To view the list of child elements in a tree-like structure, see [WLAN\_policy Schema Elements](wlan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f6d2-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f6d2-150">Requirements</span></span>



| <span data-ttu-id="3f6d2-151">需求</span><span class="sxs-lookup"><span data-stu-id="3f6d2-151">Requirement</span></span> | <span data-ttu-id="3f6d2-152">值</span><span class="sxs-lookup"><span data-stu-id="3f6d2-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f6d2-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f6d2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3f6d2-154">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f6d2-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f6d2-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f6d2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3f6d2-156">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f6d2-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




