---
title: 'DisableUserPromptForServerValidation 元素 (PEAP) '
description: '瞭解 DisableUserPromptForServerValidation (ServerValidationParameters) 元素。 指出是否應要求使用者進行伺服器驗證。 |DisableUserPromptForServerValidation 元素 (PEAP) '
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
keywords:
- DisableUserPromptForServerValidation 元素 EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976430"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a><span data-ttu-id="7ae00-106">DisableUserPromptForServerValidation (ServerValidationParameters) 元素 (PEAP) </span><span class="sxs-lookup"><span data-stu-id="7ae00-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="7ae00-107">**DisableUserPromptForServerValidation (ServerValidationParameters)** 元素指出是否應要求使用者進行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="7ae00-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="7ae00-108">如果 **DisableUserPromptForServerValidation** 為 TRUE，則 eap-tls 會執行伺服器驗證，而不需要使用者輸入;如果驗證失敗，則 EAP-TLS 會驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="7ae00-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="7ae00-109">如果 **DisableUserPromptForServerValidation** 為 FALSE，則會提示使用者輸入已驗證的伺服器憑證或名稱，或 (CA) 的根憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="7ae00-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="7ae00-110">**DisableUserPromptForServerValidation** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7ae00-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="7ae00-111">**DisableUserPromptForServerValidation** 元素是由 [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="7ae00-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae00-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ae00-112">Requirements</span></span>



| <span data-ttu-id="7ae00-113">角色</span><span class="sxs-lookup"><span data-stu-id="7ae00-113">Role</span></span> | <span data-ttu-id="7ae00-114">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="7ae00-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="7ae00-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="7ae00-115">Client</span></span><br/> | <span data-ttu-id="7ae00-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ae00-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ae00-117">伺服器</span><span class="sxs-lookup"><span data-stu-id="7ae00-117">Server</span></span><br/> | <span data-ttu-id="7ae00-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ae00-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ae00-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ae00-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ae00-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="7ae00-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7ae00-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="7ae00-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="7ae00-122">**架構實例中可能的直接父元素**</span><span class="sxs-lookup"><span data-stu-id="7ae00-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7ae00-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="7ae00-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="7ae00-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="7ae00-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="7ae00-125">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="7ae00-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7ae00-126">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="7ae00-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="7ae00-127">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="7ae00-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





