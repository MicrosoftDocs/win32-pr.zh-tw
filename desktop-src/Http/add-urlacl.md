---
title: add urlacl
description: 保留非系統管理員使用者和帳戶的指定 URL。
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- 新增 urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "103946033"
---
# <a name="add-urlacl"></a><span data-ttu-id="f8a56-104">add urlacl</span><span class="sxs-lookup"><span data-stu-id="f8a56-104">add urlacl</span></span>

<span data-ttu-id="f8a56-105">保留非系統管理員使用者和帳戶的指定 URL。</span><span class="sxs-lookup"><span data-stu-id="f8a56-105">Reserves the specified URL for non-administrator users and accounts.</span></span> <span data-ttu-id="f8a56-106">您可以使用帳戶名稱搭配接聽和委派參數，或使用安全描述項定義語言 (SDDL) 字串，來指定任意的存取控制清單 (DACL) 。</span><span class="sxs-lookup"><span data-stu-id="f8a56-106">The discretionary access control list (DACL) can be specified by using an account name with the listen and delegate parameters or by using a security descriptor definition language (SDDL) string.</span></span>

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a><span data-ttu-id="f8a56-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8a56-107">Parameters</span></span>

<dl> <span data-ttu-id="f8a56-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url =] 字串**
</dt> </span><span class="sxs-lookup"><span data-stu-id="f8a56-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> </span></span><dd>

<span data-ttu-id="f8a56-109">指定完整的 URL。</span><span class="sxs-lookup"><span data-stu-id="f8a56-109">Specifies the fully qualified URL.</span></span>

<span data-ttu-id="f8a56-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[使用者 =] 字串**
</dt> </span><span class="sxs-lookup"><span data-stu-id="f8a56-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> </span></span><dd>

<span data-ttu-id="f8a56-111">指定使用者或使用者組名。</span><span class="sxs-lookup"><span data-stu-id="f8a56-111">Specifies the user or user group name.</span></span>

</dd> <dt>

<span data-ttu-id="f8a56-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[接聽 = {yes \| 否}\]**</span><span class="sxs-lookup"><span data-stu-id="f8a56-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="f8a56-113">指定下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f8a56-113">Specifies one of the following values:</span></span>

-   <span data-ttu-id="f8a56-114">是：允許使用者註冊 Url。</span><span class="sxs-lookup"><span data-stu-id="f8a56-114">yes: Allows the user to register URLs.</span></span> <span data-ttu-id="f8a56-115">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="f8a56-115">This is the default value.</span></span>
-   <span data-ttu-id="f8a56-116">否：拒絕使用者註冊 Url。</span><span class="sxs-lookup"><span data-stu-id="f8a56-116">no: Denies the user from registering URLs.</span></span>

</dd> <dt>

<span data-ttu-id="f8a56-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate = {yes \| 否}\]**</span><span class="sxs-lookup"><span data-stu-id="f8a56-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="f8a56-118">指定下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f8a56-118">Specifies one of the following values:</span></span>

-   <span data-ttu-id="f8a56-119">是：允許使用者委派 Url。</span><span class="sxs-lookup"><span data-stu-id="f8a56-119">yes: Allows the user to delegate URLs.</span></span>
-   <span data-ttu-id="f8a56-120">否：拒絕使用者委派 Url。</span><span class="sxs-lookup"><span data-stu-id="f8a56-120">no: Denies the user from delegating URLs.</span></span> <span data-ttu-id="f8a56-121">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="f8a56-121">This is the default value.</span></span>

<span data-ttu-id="f8a56-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl =] 字串**
</dt> </span><span class="sxs-lookup"><span data-stu-id="f8a56-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> </span></span><dd>

<span data-ttu-id="f8a56-123">指定描述 DACL 的 SDDL 字串。</span><span class="sxs-lookup"><span data-stu-id="f8a56-123">Specifies the SDDL string that describes the DACL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f8a56-124">範例</span><span class="sxs-lookup"><span data-stu-id="f8a56-124">Examples</span></span>

* <span data-ttu-id="f8a56-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\ user</span><span class="sxs-lookup"><span data-stu-id="f8a56-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\user</span></span>

* <span data-ttu-id="f8a56-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span><span class="sxs-lookup"><span data-stu-id="f8a56-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span></span>

* <span data-ttu-id="f8a56-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span><span class="sxs-lookup"><span data-stu-id="f8a56-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span></span>

 
## <a name="see-also"></a><span data-ttu-id="f8a56-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8a56-128">See Also</span></span>

* [<span data-ttu-id="f8a56-129">Netsh http 命令</span><span class="sxs-lookup"><span data-stu-id="f8a56-129">Netsh http commands</span></span>](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 