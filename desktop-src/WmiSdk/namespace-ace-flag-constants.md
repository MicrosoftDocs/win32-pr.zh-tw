---
description: 下列清單列出 WMI 存取控制專案中 [旗標] 欄位的可能值 (ACE) 。
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: '命名空間 ACE 旗標常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987910"
---
# <a name="namespace-ace-flag-constants"></a><span data-ttu-id="64630-103">命名空間 ACE 旗標常數</span><span class="sxs-lookup"><span data-stu-id="64630-103">Namespace ACE Flag Constants</span></span>

<span data-ttu-id="64630-104">下列清單列出 WMI 存取控制專案中 [ **旗標** ] 欄位的可能值 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="64630-104">The following list lists the possible values of the **Flags** field in a WMI Access Control Entry (ACE).</span></span>

<dl> <dt>

<span data-ttu-id="64630-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT \_ INHERIT \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="64630-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64630-106">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="64630-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="64630-107">非容器子物件會將 ACE 繼承為有效的 ACE。</span><span class="sxs-lookup"><span data-stu-id="64630-107">Non-container child objects inherit the ACE as an effective ACE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64630-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**容器 \_ 繼承 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="64630-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64630-109">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="64630-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="64630-110">ACE 會影響子命名空間以及目前的命名空間。</span><span class="sxs-lookup"><span data-stu-id="64630-110">The ACE has an effect on child namespaces as well as the current namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64630-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**沒有 \_ 傳播 \_ 繼承 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="64630-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO\_PROPAGATE\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64630-112">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="64630-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="64630-113">ACE 僅適用于目前的命名空間和立即的子系。</span><span class="sxs-lookup"><span data-stu-id="64630-113">The ACE applies only to the current namespace and immediate children .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64630-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**\_只繼承 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="64630-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT\_ONLY\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64630-115">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="64630-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="64630-116">ACE 僅適用于子命名空間。</span><span class="sxs-lookup"><span data-stu-id="64630-116">The ACE applies only to child namespaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64630-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**繼承的 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="64630-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**INHERITED\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64630-118">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="64630-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="64630-119">用戶端不會設定這項設定，但當 ACE 的來源是父命名空間時，就會向用戶端回報。</span><span class="sxs-lookup"><span data-stu-id="64630-119">This is not set by clients, but is reported to clients when the source of an ACE is a parent namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64630-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="64630-120">Requirements</span></span>



| <span data-ttu-id="64630-121">需求</span><span class="sxs-lookup"><span data-stu-id="64630-121">Requirement</span></span> | <span data-ttu-id="64630-122">值</span><span class="sxs-lookup"><span data-stu-id="64630-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64630-123">標頭</span><span class="sxs-lookup"><span data-stu-id="64630-123">Header</span></span><br/> | <dl> <span data-ttu-id="64630-124"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="64630-124"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64630-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64630-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64630-126">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="64630-126">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="64630-127">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="64630-127">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="64630-128">建立命名空間安全性的繼承</span><span class="sxs-lookup"><span data-stu-id="64630-128">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="64630-129">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="64630-129">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




