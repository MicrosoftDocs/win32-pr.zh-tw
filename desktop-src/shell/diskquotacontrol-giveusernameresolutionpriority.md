---
description: 將指定的使用者物件放在行中，以進行名稱解析。
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: 'DiskQuotaControl. GiveUserNameResolutionPriority 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511039"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a><span data-ttu-id="0a76f-103">DiskQuotaControl. GiveUserNameResolutionPriority 方法</span><span class="sxs-lookup"><span data-stu-id="0a76f-103">DiskQuotaControl.GiveUserNameResolutionPriority method</span></span>

<span data-ttu-id="0a76f-104">將指定的使用者物件放在行中，以進行名稱解析。</span><span class="sxs-lookup"><span data-stu-id="0a76f-104">Places the specified user object next in line for name resolution.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a76f-105">語法</span><span class="sxs-lookup"><span data-stu-id="0a76f-105">Syntax</span></span>


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="0a76f-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a76f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a76f-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="0a76f-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="0a76f-108">Type： **Object**</span><span class="sxs-lookup"><span data-stu-id="0a76f-108">Type: **Object**</span></span>

<span data-ttu-id="0a76f-109">評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。</span><span class="sxs-lookup"><span data-stu-id="0a76f-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a76f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a76f-110">Return value</span></span>

<span data-ttu-id="0a76f-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a76f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a76f-112">備註</span><span class="sxs-lookup"><span data-stu-id="0a76f-112">Remarks</span></span>

<span data-ttu-id="0a76f-113">如果已啟用非同步名稱解析，則使用者物件會放置在佇列中。</span><span class="sxs-lookup"><span data-stu-id="0a76f-113">If asynchronous name resolution is enabled, user objects are placed in a queue.</span></span> <span data-ttu-id="0a76f-114">依預設，系統會依其放置在佇列中的順序來提供服務。</span><span class="sxs-lookup"><span data-stu-id="0a76f-114">By default, they are serviced in the order they are placed in the queue.</span></span> <span data-ttu-id="0a76f-115">**GiveUserNameResolutionPriority** 方法會將物件移至佇列前端，讓它成為要服務的下一個。</span><span class="sxs-lookup"><span data-stu-id="0a76f-115">The **GiveUserNameResolutionPriority** method moves an object to the front of the queue so that it is next in line to be serviced.</span></span>

<span data-ttu-id="0a76f-116">您可以使用 [**UserNameResolution**](diskquotacontrol-usernameresolution.md) 屬性來啟用非同步名稱解析。</span><span class="sxs-lookup"><span data-stu-id="0a76f-116">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to enable asynchronous name resolution.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a76f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a76f-117">Requirements</span></span>



| <span data-ttu-id="0a76f-118">需求</span><span class="sxs-lookup"><span data-stu-id="0a76f-118">Requirement</span></span> | <span data-ttu-id="0a76f-119">值</span><span class="sxs-lookup"><span data-stu-id="0a76f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a76f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a76f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a76f-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a76f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a76f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a76f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a76f-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a76f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0a76f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0a76f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a76f-125"><dt>Dskquota。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a76f-125"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="0a76f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0a76f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a76f-127"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="0a76f-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a76f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a76f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a76f-129">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="0a76f-129">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




