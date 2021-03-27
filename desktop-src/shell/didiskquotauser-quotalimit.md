---
description: 設定或取得使用者目前的配額限制。
title: DIDiskQuotaUser. QuotaLimit 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971984"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="4085c-103">DIDiskQuotaUser. QuotaLimit 屬性</span><span class="sxs-lookup"><span data-stu-id="4085c-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="4085c-104">設定或取得使用者目前的 [**配額限制**](diskquotacontrol-object.md)。</span><span class="sxs-lookup"><span data-stu-id="4085c-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="4085c-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="4085c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4085c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4085c-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="4085c-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="4085c-107">Property value</span></span>

<span data-ttu-id="4085c-108">指定或接收使用者目前配額限制的 **整數** 值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4085c-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4085c-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="4085c-109">Requirements</span></span>



| <span data-ttu-id="4085c-110">需求</span><span class="sxs-lookup"><span data-stu-id="4085c-110">Requirement</span></span> | <span data-ttu-id="4085c-111">值</span><span class="sxs-lookup"><span data-stu-id="4085c-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4085c-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4085c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4085c-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4085c-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4085c-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4085c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4085c-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4085c-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4085c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4085c-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4085c-117"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="4085c-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4085c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4085c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4085c-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="4085c-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="4085c-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="4085c-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="4085c-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="4085c-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




