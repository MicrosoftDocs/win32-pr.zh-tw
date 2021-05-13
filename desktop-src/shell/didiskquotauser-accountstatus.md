---
description: 取得使用者帳戶的狀態。
title: DIDiskQuotaUser. AccountStatus 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841649"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="2c5d6-103">DIDiskQuotaUser. AccountStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="2c5d6-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="2c5d6-104">取得使用者帳戶的狀態。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="2c5d6-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5d6-106">語法</span><span class="sxs-lookup"><span data-stu-id="2c5d6-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="2c5d6-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="2c5d6-107">Property value</span></span>

<span data-ttu-id="2c5d6-108">這個屬性可以採用下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="2c5d6-109">狀態</span><span class="sxs-lookup"><span data-stu-id="2c5d6-109">Status</span></span>            | <span data-ttu-id="2c5d6-110">值</span><span class="sxs-lookup"><span data-stu-id="2c5d6-110">Value</span></span> | <span data-ttu-id="2c5d6-111">描述</span><span class="sxs-lookup"><span data-stu-id="2c5d6-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="2c5d6-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="2c5d6-112">dqAcctResolved</span></span>    | <span data-ttu-id="2c5d6-113">0</span><span class="sxs-lookup"><span data-stu-id="2c5d6-113">0</span></span>     | <span data-ttu-id="2c5d6-114">帳戶資訊已解決。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="2c5d6-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="2c5d6-115">dqAcctUnavailable</span></span> | <span data-ttu-id="2c5d6-116">1</span><span class="sxs-lookup"><span data-stu-id="2c5d6-116">1</span></span>     | <span data-ttu-id="2c5d6-117">帳戶資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="2c5d6-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="2c5d6-118">dqAcctDeleted</span></span>     | <span data-ttu-id="2c5d6-119">2</span><span class="sxs-lookup"><span data-stu-id="2c5d6-119">2</span></span>     | <span data-ttu-id="2c5d6-120">帳戶已刪除。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="2c5d6-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="2c5d6-121">dqAcctInvalid</span></span>     | <span data-ttu-id="2c5d6-122">3</span><span class="sxs-lookup"><span data-stu-id="2c5d6-122">3</span></span>     | <span data-ttu-id="2c5d6-123">帳戶無效。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="2c5d6-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="2c5d6-124">dqAcctUnknown</span></span>     | <span data-ttu-id="2c5d6-125">4</span><span class="sxs-lookup"><span data-stu-id="2c5d6-125">4</span></span>     | <span data-ttu-id="2c5d6-126">找不到帳戶。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="2c5d6-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="2c5d6-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="2c5d6-128">5</span><span class="sxs-lookup"><span data-stu-id="2c5d6-128">5</span></span>     | <span data-ttu-id="2c5d6-129">帳戶資訊無法解析。</span><span class="sxs-lookup"><span data-stu-id="2c5d6-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="2c5d6-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c5d6-130">Requirements</span></span>



| <span data-ttu-id="2c5d6-131">需求</span><span class="sxs-lookup"><span data-stu-id="2c5d6-131">Requirement</span></span> | <span data-ttu-id="2c5d6-132">值</span><span class="sxs-lookup"><span data-stu-id="2c5d6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5d6-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c5d6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5d6-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c5d6-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c5d6-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c5d6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5d6-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c5d6-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2c5d6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2c5d6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c5d6-138"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2c5d6-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c5d6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c5d6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5d6-140">**DIDiskQuotaUser 物件**</span><span class="sxs-lookup"><span data-stu-id="2c5d6-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




