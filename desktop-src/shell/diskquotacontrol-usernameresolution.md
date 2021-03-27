---
description: 設定或取得值，這個值會控制如何將使用者安全識別碼 (SID) 解析為使用者名稱。
title: DiskQuotaControl. UserNameResolution 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: fbe079680191937f022bd45a491fad054e1a9033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972125"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="f1b8a-103">DiskQuotaControl. UserNameResolution 屬性</span><span class="sxs-lookup"><span data-stu-id="f1b8a-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="f1b8a-104">設定或取得值，這個值會控制如何將使用者安全識別碼 (SID) 解析為使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="f1b8a-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b8a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1b8a-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="f1b8a-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="f1b8a-107">Property value</span></span>

<span data-ttu-id="f1b8a-108">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="f1b8a-109">解決類型</span><span class="sxs-lookup"><span data-stu-id="f1b8a-109">Resolution Type</span></span> | <span data-ttu-id="f1b8a-110">值</span><span class="sxs-lookup"><span data-stu-id="f1b8a-110">Value</span></span> | <span data-ttu-id="f1b8a-111">描述</span><span class="sxs-lookup"><span data-stu-id="f1b8a-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b8a-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="f1b8a-112">dqResolveNone</span></span>   | <span data-ttu-id="f1b8a-113">0</span><span class="sxs-lookup"><span data-stu-id="f1b8a-113">0</span></span>     | <span data-ttu-id="f1b8a-114">請勿解析使用者名稱資訊。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="f1b8a-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="f1b8a-115">dqResolveSync</span></span>   | <span data-ttu-id="f1b8a-116">1</span><span class="sxs-lookup"><span data-stu-id="f1b8a-116">1</span></span>     | <span data-ttu-id="f1b8a-117">請稍候，正在解析名稱資訊。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="f1b8a-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="f1b8a-118">dqResolveAsync</span></span>  | <span data-ttu-id="f1b8a-119">2</span><span class="sxs-lookup"><span data-stu-id="f1b8a-119">2</span></span>     | <span data-ttu-id="f1b8a-120">請勿在解析名稱資訊時等候。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="f1b8a-121">解析名稱時，會引發 [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f1b8a-122">備註</span><span class="sxs-lookup"><span data-stu-id="f1b8a-122">Remarks</span></span>

<span data-ttu-id="f1b8a-123">這個屬性會影響 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的列舉，以及 [**AddUser**](diskquotacontrol-adduser.md) 和 [**FindUser**](diskquotacontrol-finduser.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f1b8a-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b8a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1b8a-124">Requirements</span></span>



| <span data-ttu-id="f1b8a-125">需求</span><span class="sxs-lookup"><span data-stu-id="f1b8a-125">Requirement</span></span> | <span data-ttu-id="f1b8a-126">值</span><span class="sxs-lookup"><span data-stu-id="f1b8a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b8a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1b8a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b8a-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1b8a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1b8a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1b8a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b8a-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1b8a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f1b8a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f1b8a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1b8a-132"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f1b8a-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b8a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1b8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b8a-134">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="f1b8a-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




