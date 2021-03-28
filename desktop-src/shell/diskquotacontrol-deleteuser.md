---
description: 從磁片區刪除使用者。
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: 'DiskQuotaControl. DeleteUser 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191170"
---
# <a name="diskquotacontroldeleteuser-method"></a><span data-ttu-id="0232a-103">DiskQuotaControl. DeleteUser 方法</span><span class="sxs-lookup"><span data-stu-id="0232a-103">DiskQuotaControl.DeleteUser method</span></span>

<span data-ttu-id="0232a-104">從磁片區刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="0232a-104">Deletes a user from the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="0232a-105">語法</span><span class="sxs-lookup"><span data-stu-id="0232a-105">Syntax</span></span>


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="0232a-106">參數</span><span class="sxs-lookup"><span data-stu-id="0232a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0232a-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="0232a-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="0232a-108">Type： **Object**</span><span class="sxs-lookup"><span data-stu-id="0232a-108">Type: **Object**</span></span>

<span data-ttu-id="0232a-109">評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。</span><span class="sxs-lookup"><span data-stu-id="0232a-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0232a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0232a-110">Return value</span></span>

<span data-ttu-id="0232a-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0232a-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0232a-112">備註</span><span class="sxs-lookup"><span data-stu-id="0232a-112">Remarks</span></span>

<span data-ttu-id="0232a-113">如果使用者擁有磁片區上的任何儲存空間，這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0232a-113">This method fails if the user owns any storage on the volume.</span></span> <span data-ttu-id="0232a-114">從磁片區刪除使用者之前，必須先刪除該使用者的所有存放裝置、移至另一個磁片區，或將其擁有權轉移給另一位使用者。</span><span class="sxs-lookup"><span data-stu-id="0232a-114">Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.</span></span>

## <a name="requirements"></a><span data-ttu-id="0232a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0232a-115">Requirements</span></span>



| <span data-ttu-id="0232a-116">需求</span><span class="sxs-lookup"><span data-stu-id="0232a-116">Requirement</span></span> | <span data-ttu-id="0232a-117">值</span><span class="sxs-lookup"><span data-stu-id="0232a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0232a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0232a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0232a-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0232a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0232a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0232a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0232a-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0232a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0232a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0232a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0232a-123"><dt>Dskquota。h</dt></span><span class="sxs-lookup"><span data-stu-id="0232a-123"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="0232a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0232a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0232a-125"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="0232a-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0232a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0232a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0232a-127">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="0232a-127">**AddUser**</span></span>](diskquotacontrol-adduser.md)
</dt> <dt>

[<span data-ttu-id="0232a-128">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="0232a-128">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




