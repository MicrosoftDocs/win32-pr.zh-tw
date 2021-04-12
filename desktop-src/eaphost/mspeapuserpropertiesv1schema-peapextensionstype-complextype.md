---
title: " (連接屬性的 PeapExtensionsType 複雜類型) "
description: 瞭解 PeapExtensionsType 複雜類型。 此類型可讓架構的未來增強功能。
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- PeapExtensionsType 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316486"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a><span data-ttu-id="8f61f-105"> (連接屬性的 PeapExtensionsType 複雜類型) </span><span class="sxs-lookup"><span data-stu-id="8f61f-105">PeapExtensionsType complex type (connection properties)</span></span>

<span data-ttu-id="8f61f-106">**PeapExtensionsType** 複雜型別可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="8f61f-106">The **PeapExtensionsType** complex type enables future enhancements to the schema.</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="8f61f-107">備註</span><span class="sxs-lookup"><span data-stu-id="8f61f-107">Remarks</span></span>

<span data-ttu-id="8f61f-108">**PeapExtensionsType** 複雜類型是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8f61f-108">The **PeapExtensionsType** complex type is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f61f-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f61f-109">Requirements</span></span>



| <span data-ttu-id="8f61f-110">角色</span><span class="sxs-lookup"><span data-stu-id="8f61f-110">Role</span></span> | <span data-ttu-id="8f61f-111">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="8f61f-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="8f61f-112">用戶端</span><span class="sxs-lookup"><span data-stu-id="8f61f-112">Client</span></span><br/> | <span data-ttu-id="8f61f-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f61f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f61f-114">伺服器</span><span class="sxs-lookup"><span data-stu-id="8f61f-114">Server</span></span><br/> | <span data-ttu-id="8f61f-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f61f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f61f-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f61f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f61f-117">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="8f61f-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8f61f-118">mspeapuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="8f61f-118">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





