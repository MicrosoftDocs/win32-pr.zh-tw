---
title: 連接) 元素 (連接
description: 定義每個設定設定，並將其與名稱產生關聯。 Connection 元素是選擇性的。
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- 連接元素 EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966507"
---
# <a name="connection-connections-element"></a><span data-ttu-id="897a3-105">連接) 元素 (連接</span><span class="sxs-lookup"><span data-stu-id="897a3-105">Connection (Connections) Element</span></span>

<span data-ttu-id="897a3-106">**連接 (連接)** 元素會定義每個設定設定，並將其與名稱產生關聯。</span><span class="sxs-lookup"><span data-stu-id="897a3-106">The **Connection (Connections)** element defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="897a3-107">**Connection** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="897a3-107">The **Connection** element is optional.</span></span>

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="897a3-108">**Connection** 元素是由 [**Connections**](eapconnectionpropertiesv1schema-connections-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="897a3-108">The **Connection** element is defined by the [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="897a3-109">子元素</span><span class="sxs-lookup"><span data-stu-id="897a3-109">Child elements</span></span>



| <span data-ttu-id="897a3-110">元素</span><span class="sxs-lookup"><span data-stu-id="897a3-110">Element</span></span>                                                                 | <span data-ttu-id="897a3-111">類型</span><span class="sxs-lookup"><span data-stu-id="897a3-111">Type</span></span>   | <span data-ttu-id="897a3-112">Description</span><span class="sxs-lookup"><span data-stu-id="897a3-112">Description</span></span>                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="897a3-113">**Eap**</span><span class="sxs-lookup"><span data-stu-id="897a3-113">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | <span data-ttu-id="897a3-114">識別 EAP 設定元素。</span><span class="sxs-lookup"><span data-stu-id="897a3-114">Identifies the EAP configuration element.</span></span><br/>                                                                    |
| [<span data-ttu-id="897a3-115">**名稱**</span><span class="sxs-lookup"><span data-stu-id="897a3-115">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md) | <span data-ttu-id="897a3-116">字串</span><span class="sxs-lookup"><span data-stu-id="897a3-116">string</span></span> | <span data-ttu-id="897a3-117">會捕獲所定義之連接的名稱，以協助識別多個連接。</span><span class="sxs-lookup"><span data-stu-id="897a3-117">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="897a3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="897a3-118">Requirements</span></span>



| <span data-ttu-id="897a3-119">需求</span><span class="sxs-lookup"><span data-stu-id="897a3-119">Requirement</span></span> | <span data-ttu-id="897a3-120">值</span><span class="sxs-lookup"><span data-stu-id="897a3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="897a3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="897a3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="897a3-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="897a3-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="897a3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="897a3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="897a3-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="897a3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="897a3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="897a3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="897a3-126">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="897a3-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="897a3-127">**連接**</span><span class="sxs-lookup"><span data-stu-id="897a3-127">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

<span data-ttu-id="897a3-128">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="897a3-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="897a3-129">**連接**</span><span class="sxs-lookup"><span data-stu-id="897a3-129">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[<span data-ttu-id="897a3-130">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="897a3-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="897a3-131">eapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="897a3-131">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





