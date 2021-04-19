---
title: " (TLS) 的 ServerValidationParameters 複雜類型"
description: 瞭解 ServerValidationParameters 複雜類型。 此類型包含如何執行伺服器驗證的相關資訊。 | (TLS) 的 ServerValidationParameters 複雜類型
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
keywords:
- ServerValidationParameters 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976666"
---
# <a name="servervalidationparameters-complex-type-tls"></a><span data-ttu-id="7195b-106"> (TLS) 的 ServerValidationParameters 複雜類型</span><span class="sxs-lookup"><span data-stu-id="7195b-106">ServerValidationParameters Complex Type (TLS)</span></span>

<span data-ttu-id="7195b-107">**ServerValidationParameters** 複雜類型包含如何執行伺服器驗證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7195b-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7195b-108">子元素</span><span class="sxs-lookup"><span data-stu-id="7195b-108">Child elements</span></span>



| <span data-ttu-id="7195b-109">元素</span><span class="sxs-lookup"><span data-stu-id="7195b-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="7195b-110">類型</span><span class="sxs-lookup"><span data-stu-id="7195b-110">Type</span></span>      | <span data-ttu-id="7195b-111">Description</span><span class="sxs-lookup"><span data-stu-id="7195b-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7195b-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="7195b-112">**DisableUserPromptForServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="7195b-113">boolean</span><span class="sxs-lookup"><span data-stu-id="7195b-113">boolean</span></span>   | <span data-ttu-id="7195b-114">指出是否應要求使用者進行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="7195b-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="7195b-115">如果 [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) 為 TRUE，則 eap-tls 會執行伺服器驗證，而不需要使用者輸入;如果驗證失敗，則 EAP-TLS 會驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="7195b-115">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <br/> <span data-ttu-id="7195b-116">如果 [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) 為 FALSE，則會提示使用者輸入已驗證的伺服器憑證或名稱，或 (CA) 的根憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="7195b-116">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span><br/> <span data-ttu-id="7195b-117">[**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7195b-117">The [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="7195b-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="7195b-118">**ServerNames**</span></span>](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="7195b-119">字串</span><span class="sxs-lookup"><span data-stu-id="7195b-119">string</span></span>    | <span data-ttu-id="7195b-120">代表用戶端信任的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="7195b-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="7195b-121">每個伺服器名稱會以分號分隔，而且可以使用正則運算式來表示。</span><span class="sxs-lookup"><span data-stu-id="7195b-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span><br/> <span data-ttu-id="7195b-122">[**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7195b-122">The [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="7195b-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="7195b-123">**TrustedRootCA**</span></span>](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="7195b-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="7195b-124">hexBinary</span></span> | <span data-ttu-id="7195b-125">捕捉用戶端信任的根憑證授權單位 (Ca) 的 thumb 列印。</span><span class="sxs-lookup"><span data-stu-id="7195b-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="7195b-126">Thumb 列印是包含憑證 SHA-1 雜湊的十六進位字串</span><span class="sxs-lookup"><span data-stu-id="7195b-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="7195b-127">[**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7195b-127">The [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="7195b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="7195b-128">Requirements</span></span>



| <span data-ttu-id="7195b-129">角色</span><span class="sxs-lookup"><span data-stu-id="7195b-129">Role</span></span> | <span data-ttu-id="7195b-130">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="7195b-130">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="7195b-131">用戶端</span><span class="sxs-lookup"><span data-stu-id="7195b-131">Client</span></span><br/> | <span data-ttu-id="7195b-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7195b-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7195b-133">伺服器</span><span class="sxs-lookup"><span data-stu-id="7195b-133">Server</span></span><br/> | <span data-ttu-id="7195b-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7195b-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7195b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7195b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7195b-136">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="7195b-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7195b-137">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="7195b-137">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="7195b-138">eaptlsconnectionpropertiesv1 架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="7195b-138">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





