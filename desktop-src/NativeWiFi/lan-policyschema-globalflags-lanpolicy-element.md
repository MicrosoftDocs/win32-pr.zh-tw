---
description: 包含自動設定有線網路的全域設定。
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: globalFlags (LANPolicy) 元素
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
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193671"
---
# <a name="globalflags-lanpolicy-element"></a><span data-ttu-id="f45c7-103">globalFlags (LANPolicy) 元素</span><span class="sxs-lookup"><span data-stu-id="f45c7-103">globalFlags (LANPolicy) Element</span></span>

<span data-ttu-id="f45c7-104">GlobalFlags (LANPolicy) 元素包含自動設定有線網路的全域設定。</span><span class="sxs-lookup"><span data-stu-id="f45c7-104">The globalFlags (LANPolicy) element contains the global settings for the automatic configuration of wired networks.</span></span>

``` syntax
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
```

<span data-ttu-id="f45c7-105">**GlobalFlags** 元素是由 [**LANPolicy**](lan-policyschema-lanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="f45c7-105">The **globalFlags** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f45c7-106">子元素</span><span class="sxs-lookup"><span data-stu-id="f45c7-106">Child elements</span></span>



| <span data-ttu-id="f45c7-107">元素</span><span class="sxs-lookup"><span data-stu-id="f45c7-107">Element</span></span>                                                                           | <span data-ttu-id="f45c7-108">類型</span><span class="sxs-lookup"><span data-stu-id="f45c7-108">Type</span></span>    | <span data-ttu-id="f45c7-109">Description</span><span class="sxs-lookup"><span data-stu-id="f45c7-109">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f45c7-110">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="f45c7-110">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="f45c7-111">boolean</span><span class="sxs-lookup"><span data-stu-id="f45c7-111">boolean</span></span> | <span data-ttu-id="f45c7-112">指定電腦是否使用內建的自動設定服務來管理需要第2層驗證 (（例如 802.1 X) ）之有線網路的連接。</span><span class="sxs-lookup"><span data-stu-id="f45c7-112">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f45c7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f45c7-113">Requirements</span></span>



| <span data-ttu-id="f45c7-114">需求</span><span class="sxs-lookup"><span data-stu-id="f45c7-114">Requirement</span></span> | <span data-ttu-id="f45c7-115">值</span><span class="sxs-lookup"><span data-stu-id="f45c7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f45c7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f45c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f45c7-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f45c7-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f45c7-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f45c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f45c7-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f45c7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f45c7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f45c7-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="f45c7-121">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="f45c7-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f45c7-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="f45c7-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="f45c7-123">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="f45c7-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f45c7-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="f45c7-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




