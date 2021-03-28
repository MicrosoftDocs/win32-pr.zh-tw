---
description: 重設列舉中已抓取介面的內部計數。
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'IEnumUserIdentity：： Reset 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192678"
---
# <a name="ienumuseridentityreset-method"></a><span data-ttu-id="74b74-103">IEnumUserIdentity：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="74b74-103">IEnumUserIdentity::Reset method</span></span>

<span data-ttu-id="74b74-104">\[**IEnumUserIdentity：： Reset** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="74b74-104">\[**IEnumUserIdentity::Reset** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="74b74-105">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="74b74-105">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="74b74-106">重設列舉中已抓取介面的內部計數。</span><span class="sxs-lookup"><span data-stu-id="74b74-106">Resets the internal count of retrieved interfaces in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b74-107">語法</span><span class="sxs-lookup"><span data-stu-id="74b74-107">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="74b74-108">參數</span><span class="sxs-lookup"><span data-stu-id="74b74-108">Parameters</span></span>

<span data-ttu-id="74b74-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="74b74-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74b74-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="74b74-110">Return value</span></span>

<span data-ttu-id="74b74-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="74b74-111">Type: **HRESULT**</span></span>

<span data-ttu-id="74b74-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="74b74-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74b74-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="74b74-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74b74-114">備註</span><span class="sxs-lookup"><span data-stu-id="74b74-114">Remarks</span></span>

<span data-ttu-id="74b74-115">[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。</span><span class="sxs-lookup"><span data-stu-id="74b74-115">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="74b74-116">呼叫這個方法將會重設此計數的值。</span><span class="sxs-lookup"><span data-stu-id="74b74-116">Calling this method will reset the value of this count.</span></span>

## <a name="requirements"></a><span data-ttu-id="74b74-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="74b74-117">Requirements</span></span>



| <span data-ttu-id="74b74-118">需求</span><span class="sxs-lookup"><span data-stu-id="74b74-118">Requirement</span></span> | <span data-ttu-id="74b74-119">值</span><span class="sxs-lookup"><span data-stu-id="74b74-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74b74-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74b74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74b74-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74b74-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="74b74-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74b74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74b74-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74b74-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="74b74-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="74b74-124">End of client support</span></span><br/>    | <span data-ttu-id="74b74-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="74b74-125">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="74b74-126">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="74b74-126">End of server support</span></span><br/>    | <span data-ttu-id="74b74-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74b74-127">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="74b74-128">標頭</span><span class="sxs-lookup"><span data-stu-id="74b74-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="74b74-129"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="74b74-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="74b74-130">Idl</span><span class="sxs-lookup"><span data-stu-id="74b74-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74b74-131"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="74b74-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="74b74-132">DLL</span><span class="sxs-lookup"><span data-stu-id="74b74-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b74-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74b74-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b74-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74b74-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b74-135">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="74b74-135">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="74b74-136">**IEnumUserIdentity：： Skip**</span><span class="sxs-lookup"><span data-stu-id="74b74-136">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="74b74-137">**IEnumUserIdentity：： GetCount**</span><span class="sxs-lookup"><span data-stu-id="74b74-137">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> <dt>

[<span data-ttu-id="74b74-138">**IEnumUserIdentity：： Next**</span><span class="sxs-lookup"><span data-stu-id="74b74-138">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




