---
title: Connections 元素
description: 瞭解 Connections 元素。 這個元素會收集和包含零或多個連接元素。
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Connections 元素 EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965671"
---
# <a name="connections-element"></a><span data-ttu-id="80ba9-105">Connections 元素</span><span class="sxs-lookup"><span data-stu-id="80ba9-105">Connections Element</span></span>

<span data-ttu-id="80ba9-106">**Connections** 元素會收集和包含零或多個 [**連接**](eapconnectionpropertiesv1schema-connection-connections-element.md)元素。</span><span class="sxs-lookup"><span data-stu-id="80ba9-106">The **Connections** element collects and contains zero or more [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) elements.</span></span>

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="80ba9-107">子元素</span><span class="sxs-lookup"><span data-stu-id="80ba9-107">Child elements</span></span>



| <span data-ttu-id="80ba9-108">元素</span><span class="sxs-lookup"><span data-stu-id="80ba9-108">Element</span></span>                                                                              | <span data-ttu-id="80ba9-109">類型</span><span class="sxs-lookup"><span data-stu-id="80ba9-109">Type</span></span>   | <span data-ttu-id="80ba9-110">Description</span><span class="sxs-lookup"><span data-stu-id="80ba9-110">Description</span></span>                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80ba9-111">**Eap**</span><span class="sxs-lookup"><span data-stu-id="80ba9-111">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | <span data-ttu-id="80ba9-112">識別 EAP 設定元素。</span><span class="sxs-lookup"><span data-stu-id="80ba9-112">Identifies the EAP configuration element.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="80ba9-113">**連線**</span><span class="sxs-lookup"><span data-stu-id="80ba9-113">**Connection**</span></span>](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | <span data-ttu-id="80ba9-114">定義每個設定設定，並將其與名稱產生關聯。</span><span class="sxs-lookup"><span data-stu-id="80ba9-114">Defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="80ba9-115">[**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="80ba9-115">The [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="80ba9-116">**名稱**</span><span class="sxs-lookup"><span data-stu-id="80ba9-116">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md)              | <span data-ttu-id="80ba9-117">字串</span><span class="sxs-lookup"><span data-stu-id="80ba9-117">string</span></span> | <span data-ttu-id="80ba9-118">會捕獲所定義之連接的名稱，以協助識別多個連接。</span><span class="sxs-lookup"><span data-stu-id="80ba9-118">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span><br/>                                                                     |



## <a name="remarks"></a><span data-ttu-id="80ba9-119">備註</span><span class="sxs-lookup"><span data-stu-id="80ba9-119">Remarks</span></span>

<span data-ttu-id="80ba9-120">**Connections** 元素不能透過 EAPHost api 與舊版方法搭配使用。</span><span class="sxs-lookup"><span data-stu-id="80ba9-120">The **Connections** element is not used with legacy methods via the EAPHost APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="80ba9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="80ba9-121">Requirements</span></span>



| <span data-ttu-id="80ba9-122">角色</span><span class="sxs-lookup"><span data-stu-id="80ba9-122">Role</span></span> | <span data-ttu-id="80ba9-123">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="80ba9-123">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="80ba9-124">用戶端</span><span class="sxs-lookup"><span data-stu-id="80ba9-124">Client</span></span><br/> | <span data-ttu-id="80ba9-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80ba9-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80ba9-126">伺服器</span><span class="sxs-lookup"><span data-stu-id="80ba9-126">Server</span></span><br/> | <span data-ttu-id="80ba9-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80ba9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80ba9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80ba9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ba9-129">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="80ba9-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="80ba9-130">eapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="80ba9-130">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





