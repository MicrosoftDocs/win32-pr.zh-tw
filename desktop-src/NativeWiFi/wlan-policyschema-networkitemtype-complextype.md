---
description: 指定無線網路的名稱和類型。
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: networkItemType 複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989979"
---
# <a name="networkitemtype-complex-type"></a><span data-ttu-id="c6989-103">networkItemType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="c6989-103">networkItemType Complex Type</span></span>

<span data-ttu-id="c6989-104">NetworkItemType 複雜類型會指定無線網路的名稱和類型。</span><span class="sxs-lookup"><span data-stu-id="c6989-104">The networkItemType complex type specifies the name and type of a wireless network.</span></span>

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c6989-105">子元素</span><span class="sxs-lookup"><span data-stu-id="c6989-105">Child elements</span></span>



| <span data-ttu-id="c6989-106">元素</span><span class="sxs-lookup"><span data-stu-id="c6989-106">Element</span></span>                                                                      | <span data-ttu-id="c6989-107">類型</span><span class="sxs-lookup"><span data-stu-id="c6989-107">Type</span></span>                                                                    | <span data-ttu-id="c6989-108">Description</span><span class="sxs-lookup"><span data-stu-id="c6989-108">Description</span></span>                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="c6989-109">**networkName**</span><span class="sxs-lookup"><span data-stu-id="c6989-109">**networkName**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md) | [<span data-ttu-id="c6989-110">**networkNameType**</span><span class="sxs-lookup"><span data-stu-id="c6989-110">**networkNameType**</span></span>](wlan-policyschema-networknametype-simpletype.md) | <span data-ttu-id="c6989-111">網路 (SSID) 的服務組識別元。</span><span class="sxs-lookup"><span data-stu-id="c6989-111">The service set identifier (SSID) of the network.</span></span> <br/> |
| [<span data-ttu-id="c6989-112">**networkType**</span><span class="sxs-lookup"><span data-stu-id="c6989-112">**networkType**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md) | [<span data-ttu-id="c6989-113">**networkTypeType**</span><span class="sxs-lookup"><span data-stu-id="c6989-113">**networkTypeType**</span></span>](wlan-policyschema-networktypetype-simpletype.md) | <span data-ttu-id="c6989-114">網路類型。</span><span class="sxs-lookup"><span data-stu-id="c6989-114">The network type.</span></span> <br/>                                 |



## <a name="requirements"></a><span data-ttu-id="c6989-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6989-115">Requirements</span></span>



| <span data-ttu-id="c6989-116">需求</span><span class="sxs-lookup"><span data-stu-id="c6989-116">Requirement</span></span> | <span data-ttu-id="c6989-117">值</span><span class="sxs-lookup"><span data-stu-id="c6989-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6989-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6989-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c6989-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6989-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6989-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6989-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c6989-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6989-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




