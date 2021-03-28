---
description: 清除物件的快取使用者資訊。
title: DIDiskQuotaUser 方法無效
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511043"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="4c6c0-103">DIDiskQuotaUser 方法無效</span><span class="sxs-lookup"><span data-stu-id="4c6c0-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="4c6c0-104">清除物件的快取使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6c0-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c6c0-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c6c0-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="4c6c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c6c0-106">Parameters</span></span>

<span data-ttu-id="4c6c0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4c6c0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c6c0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c6c0-108">Return value</span></span>

<span data-ttu-id="4c6c0-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4c6c0-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c6c0-110">備註</span><span class="sxs-lookup"><span data-stu-id="4c6c0-110">Remarks</span></span>

<span data-ttu-id="4c6c0-111">這個方法會清除儲存在物件快取中的使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6c0-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="4c6c0-112">下次對配額相關資訊提出要求時，物件會從 NTFS 磁片區抓取資訊並重新整理快取。</span><span class="sxs-lookup"><span data-stu-id="4c6c0-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c6c0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c6c0-113">Requirements</span></span>



| <span data-ttu-id="4c6c0-114">需求</span><span class="sxs-lookup"><span data-stu-id="4c6c0-114">Requirement</span></span> | <span data-ttu-id="4c6c0-115">值</span><span class="sxs-lookup"><span data-stu-id="4c6c0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6c0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c6c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4c6c0-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c6c0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c6c0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c6c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4c6c0-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c6c0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4c6c0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4c6c0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c6c0-121"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="4c6c0-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c6c0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c6c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c6c0-123">**DIDiskQuotaUser 物件**</span><span class="sxs-lookup"><span data-stu-id="4c6c0-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




