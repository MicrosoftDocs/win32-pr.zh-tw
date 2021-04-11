---
title: CredentialsBlob (EapHostUserCredentials) 元素
description: 當方法設定為二進位 BLOB 而非 XML 文字格式時，就會使用。
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- CredentialsBlob 元素 EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094187"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a><span data-ttu-id="23888-104">CredentialsBlob (EapHostUserCredentials) 元素</span><span class="sxs-lookup"><span data-stu-id="23888-104">CredentialsBlob (EapHostUserCredentials) Element</span></span>

<span data-ttu-id="23888-105">當方法設定是二進位 BLOB 而非 XML 文字格式時，就會使用 **CredentialsBlob (EapHostUserCredentials)** 元素。</span><span class="sxs-lookup"><span data-stu-id="23888-105">The **CredentialsBlob (EapHostUserCredentials)** element is used when the method configuration is a binary BLOB instead of in XML text format.</span></span>

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="23888-106">**CredentialsBlob** 元素是由 [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="23888-106">The **CredentialsBlob** element is defined by the [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="23888-107">備註</span><span class="sxs-lookup"><span data-stu-id="23888-107">Remarks</span></span>

<span data-ttu-id="23888-108">[**認證**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)和 **CredentialsBlob** 元素不能同時使用。</span><span class="sxs-lookup"><span data-stu-id="23888-108">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and **CredentialsBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="23888-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="23888-109">Requirements</span></span>



| <span data-ttu-id="23888-110">需求</span><span class="sxs-lookup"><span data-stu-id="23888-110">Requirement</span></span> | <span data-ttu-id="23888-111">值</span><span class="sxs-lookup"><span data-stu-id="23888-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23888-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23888-112">Minimum supported client</span></span><br/> | <span data-ttu-id="23888-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23888-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23888-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23888-114">Minimum supported server</span></span><br/> | <span data-ttu-id="23888-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23888-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23888-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23888-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="23888-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="23888-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="23888-118">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="23888-118">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

<span data-ttu-id="23888-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="23888-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="23888-120">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="23888-120">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[<span data-ttu-id="23888-121">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="23888-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="23888-122">eaphostusercredentials 架構</span><span class="sxs-lookup"><span data-stu-id="23888-122">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





