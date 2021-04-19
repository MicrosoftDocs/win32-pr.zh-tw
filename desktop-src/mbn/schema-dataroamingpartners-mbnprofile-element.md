---
description: 指定漫遊時慣用網路提供者的清單。
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: DataRoamingPartners (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970194"
---
# <a name="dataroamingpartners-mbnprofile-element"></a><span data-ttu-id="4f487-103">DataRoamingPartners (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="4f487-103">DataRoamingPartners (MBNProfile) Element</span></span>

<span data-ttu-id="4f487-104">**DataRoamingPartners (MBNProfile)** 元素會指定漫遊時慣用網路提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="4f487-104">The **DataRoamingPartners (MBNProfile)** element specifies the list of preferred network providers at the time of roaming.</span></span>

<span data-ttu-id="4f487-105">行動寬頻服務會使用此元素來選取漫遊時所提供的慣用網路。</span><span class="sxs-lookup"><span data-stu-id="4f487-105">The Mobile Broadband service uses this element to select the preferred network provide while roaming.</span></span>

<span data-ttu-id="4f487-106">元素具有下列子項目，必須至少定義一次，但可以定義多次。</span><span class="sxs-lookup"><span data-stu-id="4f487-106">The element has the following child element which must be defined at least once but can be defined multiple times.</span></span>

-   [<span data-ttu-id="4f487-107">**提供者**</span><span class="sxs-lookup"><span data-stu-id="4f487-107">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md)

<span data-ttu-id="4f487-108">此元素最多可有一次。</span><span class="sxs-lookup"><span data-stu-id="4f487-108">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="4f487-109">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="4f487-109">This element is optional.</span></span>

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4f487-110">**DataRoamingPartners** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="4f487-110">The **DataRoamingPartners** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4f487-111">子元素</span><span class="sxs-lookup"><span data-stu-id="4f487-111">Child elements</span></span>



| <span data-ttu-id="4f487-112">元素</span><span class="sxs-lookup"><span data-stu-id="4f487-112">Element</span></span>                                                         | <span data-ttu-id="4f487-113">類型</span><span class="sxs-lookup"><span data-stu-id="4f487-113">Type</span></span>                                                    | <span data-ttu-id="4f487-114">Description</span><span class="sxs-lookup"><span data-stu-id="4f487-114">Description</span></span>                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="4f487-115">**提供者**</span><span class="sxs-lookup"><span data-stu-id="4f487-115">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md) | [<span data-ttu-id="4f487-116">**providerType**</span><span class="sxs-lookup"><span data-stu-id="4f487-116">**providerType**</span></span>](schema-providertype-complextype.md) | <span data-ttu-id="4f487-117">行動電話通訊網路的名稱和提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f487-117">Name and provider ID of a cellular network.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4f487-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f487-118">Requirements</span></span>



| <span data-ttu-id="4f487-119">需求</span><span class="sxs-lookup"><span data-stu-id="4f487-119">Requirement</span></span> | <span data-ttu-id="4f487-120">值</span><span class="sxs-lookup"><span data-stu-id="4f487-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="4f487-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f487-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f487-122">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f487-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="4f487-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f487-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f487-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="4f487-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="4f487-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f487-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f487-126">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="4f487-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4f487-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="4f487-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="4f487-128">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="4f487-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4f487-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="4f487-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




