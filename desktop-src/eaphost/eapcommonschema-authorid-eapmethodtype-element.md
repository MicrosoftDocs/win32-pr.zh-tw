---
title: 作者 (EapMethodType) 元素
description: 瞭解 (EapMethodType) 元素的作者。 作者 (EapMethodType) 專案是指方法作者。
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- 作者元素 EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933622"
---
# <a name="authorid-eapmethodtype-element"></a><span data-ttu-id="e0bf0-105">作者 (EapMethodType) 元素</span><span class="sxs-lookup"><span data-stu-id="e0bf0-105">AuthorId (EapMethodType) Element</span></span>

<span data-ttu-id="e0bf0-106">作者 **(EapMethodType)** 專案是指方法作者。</span><span class="sxs-lookup"><span data-stu-id="e0bf0-106">The **AuthorId (EapMethodType)** element refers to the method author.</span></span>

<span data-ttu-id="e0bf0-107">作者是由網際網路指派的數位授權單位 (IANA) 發出的唯一號碼。</span><span class="sxs-lookup"><span data-stu-id="e0bf0-107">The AuthorId is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="e0bf0-108">**作者** 元素是由 [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="e0bf0-108">The **AuthorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0bf0-109">備註</span><span class="sxs-lookup"><span data-stu-id="e0bf0-109">Remarks</span></span>

<span data-ttu-id="e0bf0-110">針對特定方法， **作者** 和 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) 元素不需要相同的。</span><span class="sxs-lookup"><span data-stu-id="e0bf0-110">The **AuthorId** and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0bf0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0bf0-111">Requirements</span></span>



| <span data-ttu-id="e0bf0-112">角色</span><span class="sxs-lookup"><span data-stu-id="e0bf0-112">Role</span></span> | <span data-ttu-id="e0bf0-113">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="e0bf0-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="e0bf0-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="e0bf0-114">Client</span></span><br/> | <span data-ttu-id="e0bf0-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0bf0-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e0bf0-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="e0bf0-116">Server</span></span><br/> | <span data-ttu-id="e0bf0-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0bf0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0bf0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0bf0-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0bf0-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e0bf0-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e0bf0-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="e0bf0-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="e0bf0-121">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="e0bf0-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e0bf0-122">eapcommon 架構</span><span class="sxs-lookup"><span data-stu-id="e0bf0-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





