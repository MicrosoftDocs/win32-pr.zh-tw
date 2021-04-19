---
description: 包含有線區域網路原則。
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: LANPolicy 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990333"
---
# <a name="lanpolicy-element"></a><span data-ttu-id="d2554-103">LANPolicy 元素</span><span class="sxs-lookup"><span data-stu-id="d2554-103">LANPolicy Element</span></span>

<span data-ttu-id="d2554-104">LANPolicy 元素包含有線區域網路原則。</span><span class="sxs-lookup"><span data-stu-id="d2554-104">The LANPolicy element contains a wired LAN policy.</span></span> <span data-ttu-id="d2554-105">此元素是有線網路原則設定檔的唯一根項目。</span><span class="sxs-lookup"><span data-stu-id="d2554-105">This element is the unique root element for a wired network policy profile.</span></span>

<span data-ttu-id="d2554-106">**LANPolicy** 元素的目標命名空間為 `https://www.microsoft.com/networking/LAN/policy/v1` 。</span><span class="sxs-lookup"><span data-stu-id="d2554-106">The target namespace for the **LANPolicy** element is `https://www.microsoft.com/networking/LAN/policy/v1`.</span></span>

``` syntax
<xs:element name="LANPolicy">
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

## <a name="child-elements"></a><span data-ttu-id="d2554-107">子元素</span><span class="sxs-lookup"><span data-stu-id="d2554-107">Child elements</span></span>



| <span data-ttu-id="d2554-108">元素</span><span class="sxs-lookup"><span data-stu-id="d2554-108">Element</span></span>                                                                           | <span data-ttu-id="d2554-109">類型</span><span class="sxs-lookup"><span data-stu-id="d2554-109">Type</span></span>                                                     | <span data-ttu-id="d2554-110">Description</span><span class="sxs-lookup"><span data-stu-id="d2554-110">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2554-111">**描述**</span><span class="sxs-lookup"><span data-stu-id="d2554-111">**description**</span></span>](lan-policyschema-description-lanpolicy-element.md)             | [<span data-ttu-id="d2554-112">**nameType**</span><span class="sxs-lookup"><span data-stu-id="d2554-112">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="d2554-113">包含有線區域網路原則的描述。</span><span class="sxs-lookup"><span data-stu-id="d2554-113">Contains the description of a wired LAN policy.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="d2554-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="d2554-114">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="d2554-115">boolean</span><span class="sxs-lookup"><span data-stu-id="d2554-115">boolean</span></span>                                                  | <span data-ttu-id="d2554-116">指定電腦是否使用內建的自動設定服務來管理需要第2層驗證 (（例如 802.1 X) ）之有線網路的連接。</span><span class="sxs-lookup"><span data-stu-id="d2554-116">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |
| [<span data-ttu-id="d2554-117">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="d2554-117">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | <span data-ttu-id="d2554-118">包含自動設定有線網路的全域設定。</span><span class="sxs-lookup"><span data-stu-id="d2554-118">Contains the global settings for the automatic configuration of wired networks.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="d2554-119">**名字**</span><span class="sxs-lookup"><span data-stu-id="d2554-119">**name**</span></span>](lan-policyschema-name-lanpolicy-element.md)                           | [<span data-ttu-id="d2554-120">**nameType**</span><span class="sxs-lookup"><span data-stu-id="d2554-120">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="d2554-121">包含有線區域網路原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2554-121">Contains the name of a wired LAN policy.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="d2554-122">**profileList**</span><span class="sxs-lookup"><span data-stu-id="d2554-122">**profileList**</span></span>](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | <span data-ttu-id="d2554-123">包含要在網域或電腦層級套用的配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="d2554-123">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                                                                |



## <a name="remarks"></a><span data-ttu-id="d2554-124">備註</span><span class="sxs-lookup"><span data-stu-id="d2554-124">Remarks</span></span>

<span data-ttu-id="d2554-125">若要查看類似樹狀結構中子專案的清單，請參閱 [區域網路 \_ 原則架構元素](lan-policyschema-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2554-125">To view the list of child elements in a tree-like structure, see [LAN\_policy Schema Elements](lan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2554-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2554-126">Requirements</span></span>



| <span data-ttu-id="d2554-127">需求</span><span class="sxs-lookup"><span data-stu-id="d2554-127">Requirement</span></span> | <span data-ttu-id="d2554-128">值</span><span class="sxs-lookup"><span data-stu-id="d2554-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d2554-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2554-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d2554-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2554-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d2554-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2554-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d2554-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2554-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




