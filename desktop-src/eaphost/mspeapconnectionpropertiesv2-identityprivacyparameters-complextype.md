---
title: IdentityPrivacyParameters 複雜類型
description: 包含在 PEAP 驗證期間匿名身分識別使用方式的相關資訊。
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104092481"
---
# <a name="identityprivacyparameters-complex-type"></a><span data-ttu-id="661df-103">IdentityPrivacyParameters 複雜類型</span><span class="sxs-lookup"><span data-stu-id="661df-103">IdentityPrivacyParameters Complex Type</span></span>

<span data-ttu-id="661df-104">**IdentityPrivacyParameters** 複雜類型包含在 PEAP 驗證期間匿名身分識別使用方式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="661df-104">The **IdentityPrivacyParameters** complex type contains information about anonymous identity usage during PEAP authentication.</span></span>


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| <span data-ttu-id="661df-105">元素</span><span class="sxs-lookup"><span data-stu-id="661df-105">Element</span></span>                                                                                                               | <span data-ttu-id="661df-106">類型</span><span class="sxs-lookup"><span data-stu-id="661df-106">Type</span></span>    | <span data-ttu-id="661df-107">Description</span><span class="sxs-lookup"><span data-stu-id="661df-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="661df-108">**EnableIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="661df-108">**EnableIdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | <span data-ttu-id="661df-109">boolean</span><span class="sxs-lookup"><span data-stu-id="661df-109">boolean</span></span> | <span data-ttu-id="661df-110">指出是否傳送使用者的真實身分識別或匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="661df-110">Indicates whether a user's true identity or an anonymous identity is sent.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="661df-111">**AnonymousUserName**</span><span class="sxs-lookup"><span data-stu-id="661df-111">**AnonymousUserName**</span></span>](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | <span data-ttu-id="661df-112">字串</span><span class="sxs-lookup"><span data-stu-id="661df-112">string</span></span>  | <span data-ttu-id="661df-113">包含用來取代使用者真正識別的匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="661df-113">contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="661df-114">當身分 **識別** 以純文字傳送時，會在 PEAP 驗證的第一個階段傳送。</span><span class="sxs-lookup"><span data-stu-id="661df-114">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span> <span data-ttu-id="661df-115">匿名身分識別的使用方式取決於 [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="661df-115">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="661df-116">備註</span><span class="sxs-lookup"><span data-stu-id="661df-116">Remarks</span></span>

<span data-ttu-id="661df-117">IdentityPrivacyParameters 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="661df-117">The IdentityPrivacyParameters element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="661df-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="661df-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="661df-119">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="661df-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="661df-120">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="661df-120">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="661df-121">mspeapconnectionpropertiesv2 複雜類型</span><span class="sxs-lookup"><span data-stu-id="661df-121">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




