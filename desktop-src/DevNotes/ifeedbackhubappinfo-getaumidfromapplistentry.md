---
description: IFeedbackHubAppInfo：： GetAumidFromAppListEntry 方法-此 API 無法供所有應用程式使用。 除非您的應用程式是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。
ms.assetid: F205911F-7AA3-464F-A408-3BF549E1112A
title: IFeedbackHubAppInfo：： GetAumidFromAppListEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IFeedbackHubAppInfo.GetAumidFromAppListEntry
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2da6b428db156ddf18483951701216942aebbeaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089296"
---
# <a name="ifeedbackhubappinfogetaumidfromapplistentry-method"></a><span data-ttu-id="20d31-104">IFeedbackHubAppInfo：： GetAumidFromAppListEntry 方法</span><span class="sxs-lookup"><span data-stu-id="20d31-104">IFeedbackHubAppInfo::GetAumidFromAppListEntry method</span></span>

<span data-ttu-id="20d31-105">所有應用程式都無法使用此 API。</span><span class="sxs-lookup"><span data-stu-id="20d31-105">This API is not available to all apps.</span></span> <span data-ttu-id="20d31-106">除非您的應用程式是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。</span><span class="sxs-lookup"><span data-stu-id="20d31-106">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d31-107">語法</span><span class="sxs-lookup"><span data-stu-id="20d31-107">Syntax</span></span>


```C++
virtual void GetAumidFromAppListEntry(
  [in, optional]  IUnknown *appListEntry,
  [out, optional] LPWSTR   *value
);
```



## <a name="parameters"></a><span data-ttu-id="20d31-108">參數</span><span class="sxs-lookup"><span data-stu-id="20d31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20d31-109">*appListEntry* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="20d31-109">*appListEntry* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20d31-110">所有應用程式都無法使用此 API。</span><span class="sxs-lookup"><span data-stu-id="20d31-110">This API is not available to all apps.</span></span> <span data-ttu-id="20d31-111">除非您的應用程式是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。</span><span class="sxs-lookup"><span data-stu-id="20d31-111">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

</dd> <dt>

<span data-ttu-id="20d31-112">*值* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="20d31-112">*value* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20d31-113">所有應用程式都無法使用此 API。</span><span class="sxs-lookup"><span data-stu-id="20d31-113">This API is not available to all apps.</span></span> <span data-ttu-id="20d31-114">除非您的應用程式是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。</span><span class="sxs-lookup"><span data-stu-id="20d31-114">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20d31-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="20d31-115">Return value</span></span>

<span data-ttu-id="20d31-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="20d31-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="20d31-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="20d31-117">Requirements</span></span>



| <span data-ttu-id="20d31-118">需求</span><span class="sxs-lookup"><span data-stu-id="20d31-118">Requirement</span></span> | <span data-ttu-id="20d31-119">值</span><span class="sxs-lookup"><span data-stu-id="20d31-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20d31-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20d31-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20d31-121">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20d31-121">Windows 10 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="20d31-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20d31-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20d31-123">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20d31-123">Windows Server 2016 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20d31-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20d31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d31-125">**IFeedbackHubAppInfo**</span><span class="sxs-lookup"><span data-stu-id="20d31-125">**IFeedbackHubAppInfo**</span></span>](ifeebackhubappinfo.md)
</dt> </dl>

 

 




