---
description: 包含自動設定模組的全域設定 (配置) 。
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: globalFlags (WLANPolicy) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514056"
---
# <a name="globalflags-wlanpolicy-element"></a><span data-ttu-id="dd07f-103">globalFlags (WLANPolicy) 元素</span><span class="sxs-lookup"><span data-stu-id="dd07f-103">globalFlags (WLANPolicy) Element</span></span>

<span data-ttu-id="dd07f-104">GlobalFlags (WLANPolicy) 元素包含自動設定模組的全域設定 (的 [配置]) 。</span><span class="sxs-lookup"><span data-stu-id="dd07f-104">The globalFlags (WLANPolicy) element contains the global settings for the Auto Configuration Module (ACM).</span></span> <span data-ttu-id="dd07f-105">此為必要元素。</span><span class="sxs-lookup"><span data-stu-id="dd07f-105">This element is mandatory.</span></span>

``` syntax
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
```

<span data-ttu-id="dd07f-106">**GlobalFlags** 元素是由 [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="dd07f-106">The **globalFlags** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="dd07f-107">子元素</span><span class="sxs-lookup"><span data-stu-id="dd07f-107">Child elements</span></span>



| <span data-ttu-id="dd07f-108">元素</span><span class="sxs-lookup"><span data-stu-id="dd07f-108">Element</span></span>                                                                                                                    | <span data-ttu-id="dd07f-109">類型</span><span class="sxs-lookup"><span data-stu-id="dd07f-109">Type</span></span>    | <span data-ttu-id="dd07f-110">Description</span><span class="sxs-lookup"><span data-stu-id="dd07f-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd07f-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="dd07f-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="dd07f-112">boolean</span><span class="sxs-lookup"><span data-stu-id="dd07f-112">boolean</span></span> | <span data-ttu-id="dd07f-113">指定任何使用者是否可以建立所有使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="dd07f-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="dd07f-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="dd07f-114">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="dd07f-115">boolean</span><span class="sxs-lookup"><span data-stu-id="dd07f-115">boolean</span></span> | <span data-ttu-id="dd07f-116">指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。</span><span class="sxs-lookup"><span data-stu-id="dd07f-116">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="dd07f-117">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="dd07f-117">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="dd07f-118">boolean</span><span class="sxs-lookup"><span data-stu-id="dd07f-118">boolean</span></span> | <span data-ttu-id="dd07f-119">指定已拒絕的網路是否出現在 [ **連接到網路** ] 嚮導中。</span><span class="sxs-lookup"><span data-stu-id="dd07f-119">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="requirements"></a><span data-ttu-id="dd07f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd07f-120">Requirements</span></span>



| <span data-ttu-id="dd07f-121">需求</span><span class="sxs-lookup"><span data-stu-id="dd07f-121">Requirement</span></span> | <span data-ttu-id="dd07f-122">值</span><span class="sxs-lookup"><span data-stu-id="dd07f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd07f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd07f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dd07f-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd07f-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd07f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd07f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dd07f-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd07f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd07f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd07f-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="dd07f-128">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="dd07f-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="dd07f-129">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="dd07f-129">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="dd07f-130">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="dd07f-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="dd07f-131">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="dd07f-131">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




