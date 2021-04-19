---
description: 提供 Microsoft Windows HTTP Services (WinHTTP) 的事件。
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: IWinHttpRequestEvents 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985319"
---
# <a name="iwinhttprequestevents-interface"></a><span data-ttu-id="26028-103">IWinHttpRequestEvents 介面</span><span class="sxs-lookup"><span data-stu-id="26028-103">IWinHttpRequestEvents interface</span></span>

<span data-ttu-id="26028-104">**IWinHttpRequestEvents** 介面提供 [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md)的事件。</span><span class="sxs-lookup"><span data-stu-id="26028-104">The **IWinHttpRequestEvents** interface provides events for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span> <span data-ttu-id="26028-105">它只會使用事件方法。</span><span class="sxs-lookup"><span data-stu-id="26028-105">It uses only event methods.</span></span>

## <a name="members"></a><span data-ttu-id="26028-106">成員</span><span class="sxs-lookup"><span data-stu-id="26028-106">Members</span></span>

<span data-ttu-id="26028-107">**IWinHttpRequestEvents** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="26028-107">The **IWinHttpRequestEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="26028-108">**IWinHttpRequestEvents** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="26028-108">**IWinHttpRequestEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="26028-109">方法</span><span class="sxs-lookup"><span data-stu-id="26028-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26028-110">方法</span><span class="sxs-lookup"><span data-stu-id="26028-110">Methods</span></span>

<span data-ttu-id="26028-111">**IWinHttpRequestEvents** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="26028-111">The **IWinHttpRequestEvents** interface has these methods.</span></span>



| <span data-ttu-id="26028-112">方法</span><span class="sxs-lookup"><span data-stu-id="26028-112">Method</span></span>                                                                           | <span data-ttu-id="26028-113">描述</span><span class="sxs-lookup"><span data-stu-id="26028-113">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="26028-114">**OnError**</span><span class="sxs-lookup"><span data-stu-id="26028-114">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="26028-115">當應用程式中發生執行階段錯誤時發生。</span><span class="sxs-lookup"><span data-stu-id="26028-115">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="26028-116">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="26028-116">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="26028-117">當資料可從回應中取得時，就會發生。</span><span class="sxs-lookup"><span data-stu-id="26028-117">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="26028-118">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="26028-118">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="26028-119">當回應資料完成時發生。</span><span class="sxs-lookup"><span data-stu-id="26028-119">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="26028-120">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="26028-120">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="26028-121">在開始接收回應資料時發生。</span><span class="sxs-lookup"><span data-stu-id="26028-121">Occurs when the response data starts to be received.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="26028-122">備註</span><span class="sxs-lookup"><span data-stu-id="26028-122">Remarks</span></span>

<span data-ttu-id="26028-123">下列程式說明如何註冊通知。</span><span class="sxs-lookup"><span data-stu-id="26028-123">The following procedure describes how to register for notifications.</span></span>

1.  <span data-ttu-id="26028-124">藉由在 [**IWinHttpRequest**](iwinhttprequest-interface.md)物件上呼叫 **QueryInterface** 來取得 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)介面。</span><span class="sxs-lookup"><span data-stu-id="26028-124">Get an [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface by calling **QueryInterface** on an [**IWinHttpRequest**](iwinhttprequest-interface.md) object.</span></span>
2.  <span data-ttu-id="26028-125">在傳回的介面上呼叫 [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) ，並將 **IID \_ IWinHttpRequestEvents** 傳遞給 *riid*。</span><span class="sxs-lookup"><span data-stu-id="26028-125">Call [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) on the returned interface and pass **IID\_IWinHttpRequestEvents** to *riid*.</span></span>
3.  <span data-ttu-id="26028-126">呼叫所傳回連接點上的 [建議](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise)，並在執行 **IWinHttpRequestEvents** 至 *pUnk* 的物件上，將指標傳遞至 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="26028-126">Call [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) on the returned connection point and pass a pointer to an **IUnknown** interface on an object that implements **IWinHttpRequestEvents** to *pUnk*.</span></span>

<span data-ttu-id="26028-127">您可以在步驟2傳回的連接點上呼叫 [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) ，以終止通知。</span><span class="sxs-lookup"><span data-stu-id="26028-127">Notifications can be terminated by calling [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) on the connection point returned in step 2.</span></span>

<span data-ttu-id="26028-128">若要查看一些註冊 COM 通知的程式碼，請參閱 [Com 連接點](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) 一文的用戶端一節。</span><span class="sxs-lookup"><span data-stu-id="26028-128">To view some code that registers for COM notifications, see the Client section of the [COM Connection Points](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) article.</span></span>

> [!Note]  
> <span data-ttu-id="26028-129">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="26028-129">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26028-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="26028-130">Requirements</span></span>



| <span data-ttu-id="26028-131">需求</span><span class="sxs-lookup"><span data-stu-id="26028-131">Requirement</span></span> | <span data-ttu-id="26028-132">值</span><span class="sxs-lookup"><span data-stu-id="26028-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="26028-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26028-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26028-134">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26028-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="26028-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26028-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26028-136">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="26028-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="26028-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="26028-137">Redistributable</span></span><br/>          | <span data-ttu-id="26028-138">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="26028-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="26028-139">Idl</span><span class="sxs-lookup"><span data-stu-id="26028-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26028-140"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="26028-140"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26028-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26028-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26028-142">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="26028-142">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="26028-143">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="26028-143">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

