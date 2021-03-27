---
description: 當目前使用者要求切換其使用者身分識別，但在切換之前發生時呼叫。
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'IIdentityChangeNotify：： QuerySwitchIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849182"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a><span data-ttu-id="7f62c-103">IIdentityChangeNotify：： QuerySwitchIdentities 方法</span><span class="sxs-lookup"><span data-stu-id="7f62c-103">IIdentityChangeNotify::QuerySwitchIdentities method</span></span>

<span data-ttu-id="7f62c-104">\[**QuerySwitchIdentities** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7f62c-104">\[**QuerySwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7f62c-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="7f62c-106">當目前使用者要求切換其使用者身分識別，但在切換之前發生時呼叫。</span><span class="sxs-lookup"><span data-stu-id="7f62c-106">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f62c-107">語法</span><span class="sxs-lookup"><span data-stu-id="7f62c-107">Syntax</span></span>


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="7f62c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7f62c-108">Parameters</span></span>

<span data-ttu-id="7f62c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7f62c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f62c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f62c-110">Return value</span></span>

<span data-ttu-id="7f62c-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f62c-111">Type: **HRESULT**</span></span>

<span data-ttu-id="7f62c-112">參數查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="7f62c-112">Result of the switch query.</span></span> <span data-ttu-id="7f62c-113">如果應該繼續切換，請返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="7f62c-113">If the switch should proceed, return S\_OK.</span></span> <span data-ttu-id="7f62c-114">否則，會傳回 E \_ 進程 \_ 取消 \_ 的參數，表示應該中止使用者身分識別切換。</span><span class="sxs-lookup"><span data-stu-id="7f62c-114">Otherwise, return E\_PROCESS\_CANCELLED\_SWITCH to indicate that the user identity switch should be aborted.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f62c-115">備註</span><span class="sxs-lookup"><span data-stu-id="7f62c-115">Remarks</span></span>

<span data-ttu-id="7f62c-116">當使用者要求切換身分識別時，您可以執行此方法來為您的應用程式提供自訂行為。</span><span class="sxs-lookup"><span data-stu-id="7f62c-116">You may implement this method to provide custom behavior for your application when a user requests that identities be switched.</span></span> <span data-ttu-id="7f62c-117">您可以藉由傳回「E 進程取消」參數的值，停止暫止的身分識別切換 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7f62c-117">You can stop the pending identity switch by returning the value E\_PROCESS\_CANCELLED\_SWITCH.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f62c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f62c-118">Requirements</span></span>



| <span data-ttu-id="7f62c-119">需求</span><span class="sxs-lookup"><span data-stu-id="7f62c-119">Requirement</span></span> | <span data-ttu-id="7f62c-120">值</span><span class="sxs-lookup"><span data-stu-id="7f62c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f62c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f62c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f62c-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7f62c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f62c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f62c-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7f62c-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7f62c-125">End of client support</span></span><br/>    | <span data-ttu-id="7f62c-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7f62c-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="7f62c-127">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7f62c-127">End of server support</span></span><br/>    | <span data-ttu-id="7f62c-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f62c-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="7f62c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7f62c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f62c-130"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f62c-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f62c-131">Idl</span><span class="sxs-lookup"><span data-stu-id="7f62c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f62c-132"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f62c-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7f62c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7f62c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f62c-134"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f62c-134"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7f62c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f62c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f62c-136">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="7f62c-136">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="7f62c-137">**IIdentityChangeNotify::SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="7f62c-137">**IIdentityChangeNotify::SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




