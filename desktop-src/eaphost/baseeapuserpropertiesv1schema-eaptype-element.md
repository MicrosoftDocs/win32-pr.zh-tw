---
title: 'EapType 元素 (基底使用者屬性) '
description: '瞭解 EapType 元素。 這個元素會在 Eap 專案內捕獲特定方法的設定。 |EapType 元素 (基底使用者屬性) '
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974811"
---
# <a name="eaptype-element-base-user-properties"></a><span data-ttu-id="e6362-106">EapType 元素 (基底使用者屬性) </span><span class="sxs-lookup"><span data-stu-id="e6362-106">EapType element (base user properties)</span></span>

<span data-ttu-id="e6362-107">**EapType** 元素會在 Eap 專案內捕獲特定方法的設定。</span><span class="sxs-lookup"><span data-stu-id="e6362-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="e6362-108">備註</span><span class="sxs-lookup"><span data-stu-id="e6362-108">Remarks</span></span>

<span data-ttu-id="e6362-109">**EapType** 元素是抽象的;每個方法都必須定義和使用實例檔中的衍生元素。</span><span class="sxs-lookup"><span data-stu-id="e6362-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6362-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6362-110">Requirements</span></span>



| <span data-ttu-id="e6362-111">角色</span><span class="sxs-lookup"><span data-stu-id="e6362-111">Role</span></span> | <span data-ttu-id="e6362-112">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="e6362-112">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6362-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="e6362-113">Client</span></span><br/> | <span data-ttu-id="e6362-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6362-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6362-115">伺服器</span><span class="sxs-lookup"><span data-stu-id="e6362-115">Server</span></span><br/> | <span data-ttu-id="e6362-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6362-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6362-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6362-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6362-118">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="e6362-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e6362-119">baseeapuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="e6362-119">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





