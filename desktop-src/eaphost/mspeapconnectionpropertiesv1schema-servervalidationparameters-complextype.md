---
title: " (PEAP) 的 ServerValidationParameters 複雜類型"
description: 瞭解 ServerValidationParameters 複雜類型。 此類型包含如何執行伺服器驗證的相關資訊。 | (PEAP) 的 ServerValidationParameters 複雜類型
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
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
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945788"
---
# <a name="servervalidationparameters-complex-type-peap"></a><span data-ttu-id="50ea7-106"> (PEAP) 的 ServerValidationParameters 複雜類型</span><span class="sxs-lookup"><span data-stu-id="50ea7-106">ServerValidationParameters complex type (PEAP)</span></span>

<span data-ttu-id="50ea7-107">**ServerValidationParameters** 複雜類型包含如何執行伺服器驗證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="50ea7-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="50ea7-108">子元素</span><span class="sxs-lookup"><span data-stu-id="50ea7-108">Child elements</span></span>



| <span data-ttu-id="50ea7-109">元素</span><span class="sxs-lookup"><span data-stu-id="50ea7-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="50ea7-110">類型</span><span class="sxs-lookup"><span data-stu-id="50ea7-110">Type</span></span>        | <span data-ttu-id="50ea7-111">Description</span><span class="sxs-lookup"><span data-stu-id="50ea7-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50ea7-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="50ea7-112">**DisableUserPromptForServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="50ea7-113">boolean</span><span class="sxs-lookup"><span data-stu-id="50ea7-113">boolean</span></span>     | <span data-ttu-id="50ea7-114">指出是否應要求使用者進行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="50ea7-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="50ea7-115">如果 [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) 為 TRUE，則 PEAP 會執行伺服器驗證，而不需要使用者輸入;如果驗證失敗，PEAP 會驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="50ea7-115">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then PEAP performs the server validation without user input; if the validation fails, PEAP fails the authentication.</span></span><br/> <span data-ttu-id="50ea7-116">如果 [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) 為 FALSE，則會提示使用者輸入已驗證的伺服器憑證或名稱，或 (CA) 的根憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="50ea7-116">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certification authority (CA).</span></span><br/> <span data-ttu-id="50ea7-117">[**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="50ea7-117">The [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="50ea7-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="50ea7-118">**ServerNames**</span></span>](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="50ea7-119">complextype</span><span class="sxs-lookup"><span data-stu-id="50ea7-119">complextype</span></span> | <span data-ttu-id="50ea7-120">代表用戶端信任的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="50ea7-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="50ea7-121">每個伺服器名稱會以分號分隔，而且可以使用正則運算式來表示。</span><span class="sxs-lookup"><span data-stu-id="50ea7-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <br/> <span data-ttu-id="50ea7-122">[**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="50ea7-122">The [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="50ea7-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="50ea7-123">**TrustedRootCA**</span></span>](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="50ea7-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="50ea7-124">hexBinary</span></span>   | <span data-ttu-id="50ea7-125">捕捉用戶端信任的根憑證授權單位 (Ca) 的 thumb 列印。</span><span class="sxs-lookup"><span data-stu-id="50ea7-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="50ea7-126">Thumb 列印是包含憑證 SHA-1 雜湊的十六進位字串</span><span class="sxs-lookup"><span data-stu-id="50ea7-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="50ea7-127">[**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="50ea7-127">The [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a><span data-ttu-id="50ea7-128">屬性</span><span class="sxs-lookup"><span data-stu-id="50ea7-128">Attributes</span></span>



| <span data-ttu-id="50ea7-129">名稱</span><span class="sxs-lookup"><span data-stu-id="50ea7-129">Name</span></span>                    | <span data-ttu-id="50ea7-130">類型</span><span class="sxs-lookup"><span data-stu-id="50ea7-130">Type</span></span>    | <span data-ttu-id="50ea7-131">Description</span><span class="sxs-lookup"><span data-stu-id="50ea7-131">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ea7-132">PerformServerValidation</span><span class="sxs-lookup"><span data-stu-id="50ea7-132">PerformServerValidation</span></span> | <span data-ttu-id="50ea7-133">boolean</span><span class="sxs-lookup"><span data-stu-id="50ea7-133">boolean</span></span> | <span data-ttu-id="50ea7-134">Windows 7 或更新版本：指出是否執行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="50ea7-134">Windows 7 or later: Indicates whether server validation is performed.</span></span> <span data-ttu-id="50ea7-135">[**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="50ea7-135">The [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="50ea7-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="50ea7-136">Requirements</span></span>



| <span data-ttu-id="50ea7-137">角色</span><span class="sxs-lookup"><span data-stu-id="50ea7-137">Role</span></span> | <span data-ttu-id="50ea7-138">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="50ea7-138">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="50ea7-139">用戶端</span><span class="sxs-lookup"><span data-stu-id="50ea7-139">Client</span></span><br/> | <span data-ttu-id="50ea7-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50ea7-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50ea7-141">伺服器</span><span class="sxs-lookup"><span data-stu-id="50ea7-141">Server</span></span><br/> | <span data-ttu-id="50ea7-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50ea7-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50ea7-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50ea7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ea7-144">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="50ea7-144">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="50ea7-145">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="50ea7-145">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="50ea7-146">mspeapconnectionpropertiesv1 架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="50ea7-146">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="50ea7-147">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="50ea7-147">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





