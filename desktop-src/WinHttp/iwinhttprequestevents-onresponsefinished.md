---
description: 當回應資料完成時發生。
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: IWinHttpRequestEvents：： OnResponseFinished 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976968"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a><span data-ttu-id="d3318-103">IWinHttpRequestEvents：： OnResponseFinished 事件</span><span class="sxs-lookup"><span data-stu-id="d3318-103">IWinHttpRequestEvents::OnResponseFinished event</span></span>

<span data-ttu-id="d3318-104">完成回應資料時，就會發生 **OnResponseFinished** 事件。</span><span class="sxs-lookup"><span data-stu-id="d3318-104">The **OnResponseFinished** event occurs when the response data is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3318-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3318-105">Syntax</span></span>


```C++
void OnResponseFinished();
```



## <a name="parameters"></a><span data-ttu-id="d3318-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3318-106">Parameters</span></span>

<span data-ttu-id="d3318-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d3318-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3318-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3318-108">Return value</span></span>

<span data-ttu-id="d3318-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d3318-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3318-110">備註</span><span class="sxs-lookup"><span data-stu-id="d3318-110">Remarks</span></span>

<span data-ttu-id="d3318-111">此事件表示已收到所有與最近要求相關的回應資料。</span><span class="sxs-lookup"><span data-stu-id="d3318-111">This event signals that all of the response data that pertains to the most recent request has been received.</span></span> <span data-ttu-id="d3318-112">在下一個要求之前， [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md)不會再次發生。</span><span class="sxs-lookup"><span data-stu-id="d3318-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) does not occur again until the next request.</span></span>

> [!Note]  
> <span data-ttu-id="d3318-113">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="d3318-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3318-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3318-114">Requirements</span></span>



| <span data-ttu-id="d3318-115">需求</span><span class="sxs-lookup"><span data-stu-id="d3318-115">Requirement</span></span> | <span data-ttu-id="d3318-116">值</span><span class="sxs-lookup"><span data-stu-id="d3318-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3318-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3318-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3318-118">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3318-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="d3318-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3318-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3318-120">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="d3318-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="d3318-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d3318-121">Redistributable</span></span><br/>          | <span data-ttu-id="d3318-122">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d3318-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="d3318-123">Idl</span><span class="sxs-lookup"><span data-stu-id="d3318-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3318-124"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3318-124"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3318-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3318-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3318-126">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="d3318-126">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="d3318-127">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d3318-127">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="d3318-128">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="d3318-128">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




