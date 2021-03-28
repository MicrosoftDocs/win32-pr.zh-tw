---
description: 當已解析 DIDiskQuotaUser 物件的名稱資訊時發生。
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: 'OnUserNameChanged 函式 (Dskquota) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319551"
---
# <a name="onusernamechanged-function"></a><span data-ttu-id="52c6c-103">OnUserNameChanged 函式</span><span class="sxs-lookup"><span data-stu-id="52c6c-103">OnUserNameChanged function</span></span>

<span data-ttu-id="52c6c-104">當已解析 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的名稱資訊時發生。</span><span class="sxs-lookup"><span data-stu-id="52c6c-104">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span>

## <a name="parameters"></a><span data-ttu-id="52c6c-105">參數</span><span class="sxs-lookup"><span data-stu-id="52c6c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52c6c-106">*oUser*</span><span class="sxs-lookup"><span data-stu-id="52c6c-106">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="52c6c-107">物件，該 **物件** 會評估為與已解析其名稱之使用者相關聯的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="52c6c-107">The **Object** that evaluates to the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the user whose name has been resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52c6c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="52c6c-108">Return value</span></span>

<span data-ttu-id="52c6c-109">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="52c6c-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c6c-110">備註</span><span class="sxs-lookup"><span data-stu-id="52c6c-110">Remarks</span></span>

<span data-ttu-id="52c6c-111">當用戶端 [**列舉使用者**](didiskquotauser-object.md)或呼叫 [**AddUser**](diskquotacontrol-adduser.md) 或 [**FindUser**](diskquotacontrol-finduser.md) 方法時，必須將使用者名稱解析為相關聯的安全識別碼 (SID) 。</span><span class="sxs-lookup"><span data-stu-id="52c6c-111">When a client [**enumerates users**](didiskquotauser-object.md), or calls the [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md) method, the user name must be resolved to the associated security ID (SID).</span></span> <span data-ttu-id="52c6c-112">因為這個程式可能很耗時，所以用戶端可以在背景執行緒上以非同步方式進行名稱解析。</span><span class="sxs-lookup"><span data-stu-id="52c6c-112">Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread.</span></span> <span data-ttu-id="52c6c-113">當使用者的名稱解析時， [**DiskQuotaControl**](diskquotacontrol-object.md) 物件會引發 **OnUserNameChanged** 事件來通知其用戶端。</span><span class="sxs-lookup"><span data-stu-id="52c6c-113">When a user's name is resolved, the [**DiskQuotaControl**](diskquotacontrol-object.md) object notifies its client by firing the **OnUserNameChanged** event.</span></span> <span data-ttu-id="52c6c-114">與使用者相關聯的 **DIDiskQuotaUser** 物件會以參數形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="52c6c-114">A **DIDiskQuotaUser** object associated with the user is passed as a parameter.</span></span> <span data-ttu-id="52c6c-115">此物件可讓用戶端修改使用者的配額設定。</span><span class="sxs-lookup"><span data-stu-id="52c6c-115">This object allows the client to modify the user's quota settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c6c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="52c6c-116">Requirements</span></span>



| <span data-ttu-id="52c6c-117">需求</span><span class="sxs-lookup"><span data-stu-id="52c6c-117">Requirement</span></span> | <span data-ttu-id="52c6c-118">值</span><span class="sxs-lookup"><span data-stu-id="52c6c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52c6c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52c6c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52c6c-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52c6c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52c6c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52c6c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52c6c-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52c6c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="52c6c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="52c6c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52c6c-124"><dt>Dskquota。h</dt></span><span class="sxs-lookup"><span data-stu-id="52c6c-124"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="52c6c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="52c6c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52c6c-126"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="52c6c-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c6c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52c6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c6c-128">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="52c6c-128">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




