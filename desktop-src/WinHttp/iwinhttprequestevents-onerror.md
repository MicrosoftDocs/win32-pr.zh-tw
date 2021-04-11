---
description: 當應用程式中發生執行階段錯誤時發生。
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: IWinHttpRequestEvents：： OnError 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945187"
---
# <a name="iwinhttprequesteventsonerror-event"></a><span data-ttu-id="ef31d-103">IWinHttpRequestEvents：： OnError 事件</span><span class="sxs-lookup"><span data-stu-id="ef31d-103">IWinHttpRequestEvents::OnError event</span></span>

<span data-ttu-id="ef31d-104">當應用程式中發生執行階段錯誤時，就會發生 **OnError** 事件。</span><span class="sxs-lookup"><span data-stu-id="ef31d-104">The **OnError** event occurs when there is a run-time error in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef31d-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef31d-105">Syntax</span></span>


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="ef31d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef31d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef31d-107">*ErrorNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef31d-107">*ErrorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef31d-108">接收錯誤的數值。</span><span class="sxs-lookup"><span data-stu-id="ef31d-108">Receives the numerical value of the error.</span></span> <span data-ttu-id="ef31d-109">此錯誤號碼的較低16位會對應到 [**錯誤訊息**](error-messages.md)中所列的其中一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="ef31d-109">The lower 16 bits of this error number corresponds to one of the errors listed in [**Error Messages**](error-messages.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef31d-110">*ErrorDescription* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef31d-110">*ErrorDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef31d-111">指定所發生錯誤的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ef31d-111">Specifies a short description of the error which occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef31d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef31d-112">Return value</span></span>

<span data-ttu-id="ef31d-113">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ef31d-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef31d-114">備註</span><span class="sxs-lookup"><span data-stu-id="ef31d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ef31d-115">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="ef31d-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef31d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef31d-116">Requirements</span></span>



| <span data-ttu-id="ef31d-117">需求</span><span class="sxs-lookup"><span data-stu-id="ef31d-117">Requirement</span></span> | <span data-ttu-id="ef31d-118">值</span><span class="sxs-lookup"><span data-stu-id="ef31d-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef31d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef31d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef31d-120">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef31d-120">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="ef31d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef31d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef31d-122">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="ef31d-122">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="ef31d-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ef31d-123">Redistributable</span></span><br/>          | <span data-ttu-id="ef31d-124">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ef31d-124">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="ef31d-125">Idl</span><span class="sxs-lookup"><span data-stu-id="ef31d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef31d-126"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef31d-126"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef31d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef31d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef31d-128">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="ef31d-128">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="ef31d-129">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ef31d-129">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="ef31d-130">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="ef31d-130">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




