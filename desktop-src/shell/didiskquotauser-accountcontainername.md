---
description: 取得使用者帳戶容器的名稱。
title: DIDiskQuotaUser. AccountContainerName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843349"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="797d2-103">DIDiskQuotaUser. AccountContainerName 屬性</span><span class="sxs-lookup"><span data-stu-id="797d2-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="797d2-104">取得使用者帳戶容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="797d2-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="797d2-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="797d2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="797d2-106">語法</span><span class="sxs-lookup"><span data-stu-id="797d2-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="797d2-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="797d2-107">Property value</span></span>

<span data-ttu-id="797d2-108">設定為使用者帳戶容器名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="797d2-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="797d2-109">備註</span><span class="sxs-lookup"><span data-stu-id="797d2-109">Remarks</span></span>

<span data-ttu-id="797d2-110">針對沒有目錄服務資訊的帳戶，此屬性包含功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="797d2-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="797d2-111">若為具有目錄服務資訊的帳戶，此屬性會包含已移除終止物件名稱的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="797d2-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="797d2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="797d2-112">Requirements</span></span>



| <span data-ttu-id="797d2-113">需求</span><span class="sxs-lookup"><span data-stu-id="797d2-113">Requirement</span></span> | <span data-ttu-id="797d2-114">值</span><span class="sxs-lookup"><span data-stu-id="797d2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="797d2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="797d2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="797d2-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="797d2-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="797d2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="797d2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="797d2-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="797d2-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="797d2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="797d2-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="797d2-120"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="797d2-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="797d2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="797d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="797d2-122">**DIDiskQuotaUser 物件**</span><span class="sxs-lookup"><span data-stu-id="797d2-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




