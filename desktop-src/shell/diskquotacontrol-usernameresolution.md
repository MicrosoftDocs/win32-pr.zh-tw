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
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841459"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="87203-103">DiskQuotaControl. UserNameResolution 屬性</span><span class="sxs-lookup"><span data-stu-id="87203-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="87203-104">設定或取得值，這個值會控制如何將使用者安全識別碼 (SID) 解析為使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="87203-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="87203-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="87203-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="87203-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="87203-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="87203-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="87203-107">Property value</span></span>

<span data-ttu-id="87203-108">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="87203-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="87203-109">解決類型</span><span class="sxs-lookup"><span data-stu-id="87203-109">Resolution Type</span></span> | <span data-ttu-id="87203-110">值</span><span class="sxs-lookup"><span data-stu-id="87203-110">Value</span></span> | <span data-ttu-id="87203-111">描述</span><span class="sxs-lookup"><span data-stu-id="87203-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87203-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="87203-112">dqResolveNone</span></span>   | <span data-ttu-id="87203-113">0</span><span class="sxs-lookup"><span data-stu-id="87203-113">0</span></span>     | <span data-ttu-id="87203-114">請勿解析使用者名稱資訊。</span><span class="sxs-lookup"><span data-stu-id="87203-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="87203-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="87203-115">dqResolveSync</span></span>   | <span data-ttu-id="87203-116">1</span><span class="sxs-lookup"><span data-stu-id="87203-116">1</span></span>     | <span data-ttu-id="87203-117">請稍候，正在解析名稱資訊。</span><span class="sxs-lookup"><span data-stu-id="87203-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="87203-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="87203-118">dqResolveAsync</span></span>  | <span data-ttu-id="87203-119">2</span><span class="sxs-lookup"><span data-stu-id="87203-119">2</span></span>     | <span data-ttu-id="87203-120">請勿在解析名稱資訊時等候。</span><span class="sxs-lookup"><span data-stu-id="87203-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="87203-121">解析名稱時，會引發 [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="87203-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="87203-122">備註</span><span class="sxs-lookup"><span data-stu-id="87203-122">Remarks</span></span>

<span data-ttu-id="87203-123">這個屬性會影響 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的列舉，以及 [**AddUser**](diskquotacontrol-adduser.md) 和 [**FindUser**](diskquotacontrol-finduser.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="87203-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="87203-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="87203-124">Requirements</span></span>



| <span data-ttu-id="87203-125">需求</span><span class="sxs-lookup"><span data-stu-id="87203-125">Requirement</span></span> | <span data-ttu-id="87203-126">值</span><span class="sxs-lookup"><span data-stu-id="87203-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87203-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87203-127">Minimum supported client</span></span><br/> | <span data-ttu-id="87203-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87203-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87203-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87203-129">Minimum supported server</span></span><br/> | <span data-ttu-id="87203-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87203-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="87203-131">DLL</span><span class="sxs-lookup"><span data-stu-id="87203-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87203-132"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="87203-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87203-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87203-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87203-134">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="87203-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




