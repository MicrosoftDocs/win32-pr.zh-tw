---
title: emptyString 簡單類型
description: 深入瞭解未使用的 emptyString 簡單類型。 查看需求並查看其他可用的資源。
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- emptyString 簡單類型 EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 756c8976c8b989cf77be921491770fcff9ea62d5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024115"
---
# <a name="emptystring-simple-type"></a><span data-ttu-id="3f48a-105">emptyString 簡單類型</span><span class="sxs-lookup"><span data-stu-id="3f48a-105">emptyString Simple Type</span></span>

<span data-ttu-id="3f48a-106">**EmptyString** 簡單類型未使用中。</span><span class="sxs-lookup"><span data-stu-id="3f48a-106">The **emptyString** simple type is not in use.</span></span>

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="3f48a-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f48a-107">Requirements</span></span>



| <span data-ttu-id="3f48a-108">角色</span><span class="sxs-lookup"><span data-stu-id="3f48a-108">Role</span></span> | <span data-ttu-id="3f48a-109">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="3f48a-109">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f48a-110">用戶端</span><span class="sxs-lookup"><span data-stu-id="3f48a-110">Client</span></span><br/> | <span data-ttu-id="3f48a-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f48a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f48a-112">伺服器</span><span class="sxs-lookup"><span data-stu-id="3f48a-112">Server</span></span><br/> | <span data-ttu-id="3f48a-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f48a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f48a-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f48a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f48a-115">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="3f48a-115">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3f48a-116">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="3f48a-116">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3f48a-117">eaptlsconnectionpropertiesv1 架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="3f48a-117">eaptlsconnectionpropertiesv1 Schema Simple Types</span></span>](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





