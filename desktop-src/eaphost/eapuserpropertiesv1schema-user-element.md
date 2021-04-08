---
title: User 元素
description: 瞭解 User 元素。 透過 EAPHost Api 使用舊版方法時，不會使用這個元素。
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- 使用者元素 EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683123"
---
# <a name="user-element"></a><span data-ttu-id="9a216-105">User 元素</span><span class="sxs-lookup"><span data-stu-id="9a216-105">User Element</span></span>

<span data-ttu-id="9a216-106">透過 EAPHost Api 使用舊版方法時，不會使用 **使用者** 元素。</span><span class="sxs-lookup"><span data-stu-id="9a216-106">The **User** element is not used when using legacy methods via the EAPHost APIs.</span></span>

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="9a216-107">子元素</span><span class="sxs-lookup"><span data-stu-id="9a216-107">Child elements</span></span>



| <span data-ttu-id="9a216-108">元素</span><span class="sxs-lookup"><span data-stu-id="9a216-108">Element</span></span>                                                  | <span data-ttu-id="9a216-109">類型</span><span class="sxs-lookup"><span data-stu-id="9a216-109">Type</span></span> | <span data-ttu-id="9a216-110">Description</span><span class="sxs-lookup"><span data-stu-id="9a216-110">Description</span></span>                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="9a216-111">**Eap**</span><span class="sxs-lookup"><span data-stu-id="9a216-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md) |      | <span data-ttu-id="9a216-112">捕捉方法類型和方法特定的認證資訊。</span><span class="sxs-lookup"><span data-stu-id="9a216-112">Captures the method type and method specific credential information.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9a216-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a216-113">Requirements</span></span>



| <span data-ttu-id="9a216-114">角色</span><span class="sxs-lookup"><span data-stu-id="9a216-114">Role</span></span> | <span data-ttu-id="9a216-115">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="9a216-115">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="9a216-116">用戶端</span><span class="sxs-lookup"><span data-stu-id="9a216-116">Client</span></span><br/> | <span data-ttu-id="9a216-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a216-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a216-118">伺服器</span><span class="sxs-lookup"><span data-stu-id="9a216-118">Server</span></span><br/> | <span data-ttu-id="9a216-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a216-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a216-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a216-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a216-121">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="9a216-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9a216-122">eapuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="9a216-122">eapuserpropertiesv1 Schema</span></span>](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





