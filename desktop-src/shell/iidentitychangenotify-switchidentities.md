---
description: 當使用者身分識別切換時呼叫。
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'IIdentityChangeNotify：： SwitchIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991522"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a><span data-ttu-id="017cc-103">IIdentityChangeNotify：： SwitchIdentities 方法</span><span class="sxs-lookup"><span data-stu-id="017cc-103">IIdentityChangeNotify::SwitchIdentities method</span></span>

<span data-ttu-id="017cc-104">\[**SwitchIdentities** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="017cc-104">\[**SwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="017cc-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="017cc-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="017cc-106">當使用者身分識別切換時呼叫。</span><span class="sxs-lookup"><span data-stu-id="017cc-106">Called when user identities are switched.</span></span>

## <a name="syntax"></a><span data-ttu-id="017cc-107">語法</span><span class="sxs-lookup"><span data-stu-id="017cc-107">Syntax</span></span>


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="017cc-108">參數</span><span class="sxs-lookup"><span data-stu-id="017cc-108">Parameters</span></span>

<span data-ttu-id="017cc-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="017cc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="017cc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="017cc-110">Return value</span></span>

<span data-ttu-id="017cc-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="017cc-111">Type: **HRESULT**</span></span>

<span data-ttu-id="017cc-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="017cc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="017cc-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="017cc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="017cc-114">備註</span><span class="sxs-lookup"><span data-stu-id="017cc-114">Remarks</span></span>

<span data-ttu-id="017cc-115">當使用者已成功切換身分識別時，您可以執行此方法來為您的應用程式提供自訂行為。</span><span class="sxs-lookup"><span data-stu-id="017cc-115">You may implement this method to provide custom behavior for your application when a user has successfully switched identities.</span></span> <span data-ttu-id="017cc-116">若要在發生使用者身分識別切換之前提供自訂行為，請執行 [**IIdentityChangeNotify：： QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="017cc-116">To provide custom behavior before a user identity switch occurs, implement the [**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="017cc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="017cc-117">Requirements</span></span>



| <span data-ttu-id="017cc-118">需求</span><span class="sxs-lookup"><span data-stu-id="017cc-118">Requirement</span></span> | <span data-ttu-id="017cc-119">值</span><span class="sxs-lookup"><span data-stu-id="017cc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="017cc-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="017cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="017cc-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="017cc-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="017cc-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="017cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="017cc-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="017cc-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="017cc-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="017cc-124">End of client support</span></span><br/>    | <span data-ttu-id="017cc-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="017cc-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="017cc-126">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="017cc-126">End of server support</span></span><br/>    | <span data-ttu-id="017cc-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="017cc-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="017cc-128">標頭</span><span class="sxs-lookup"><span data-stu-id="017cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="017cc-129"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="017cc-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="017cc-130">Idl</span><span class="sxs-lookup"><span data-stu-id="017cc-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="017cc-131"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="017cc-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="017cc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="017cc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="017cc-133"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="017cc-133"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="017cc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="017cc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017cc-135">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="017cc-135">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="017cc-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="017cc-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




