---
title: 'EapType 元素 (v1 架構連接屬性) '
description: '瞭解 EapType 元素。 這個元素會在 Eap 專案內捕獲特定方法的設定。 |EapType 元素 (v1 架構連接屬性) '
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- EapType 元素 EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696390"
---
# <a name="eaptype-element-v1-schema-connection-property"></a><span data-ttu-id="f2a8f-106">EapType 元素 (v1 架構連接屬性) </span><span class="sxs-lookup"><span data-stu-id="f2a8f-106">EapType Element (v1 schema connection property)</span></span>

<span data-ttu-id="f2a8f-107">**EapType** 元素會在 Eap 專案內捕獲特定方法的設定。</span><span class="sxs-lookup"><span data-stu-id="f2a8f-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="f2a8f-108">備註</span><span class="sxs-lookup"><span data-stu-id="f2a8f-108">Remarks</span></span>

<span data-ttu-id="f2a8f-109">**EapType** 元素是抽象的;每個方法都必須定義和使用實例檔中的衍生元素。</span><span class="sxs-lookup"><span data-stu-id="f2a8f-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a8f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2a8f-110">Requirements</span></span>



| <span data-ttu-id="f2a8f-111">角色</span><span class="sxs-lookup"><span data-stu-id="f2a8f-111">Role</span></span> | <span data-ttu-id="f2a8f-112">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="f2a8f-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f2a8f-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="f2a8f-113">Client</span></span><br/> | <span data-ttu-id="f2a8f-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2a8f-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2a8f-115">伺服器</span><span class="sxs-lookup"><span data-stu-id="f2a8f-115">Server</span></span><br/> | <span data-ttu-id="f2a8f-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2a8f-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2a8f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2a8f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a8f-118">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="f2a8f-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f2a8f-119">baseeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="f2a8f-119">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





