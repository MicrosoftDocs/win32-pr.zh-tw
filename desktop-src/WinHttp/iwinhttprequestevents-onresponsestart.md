---
description: 在開始接收回應資料時發生。
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: IWinHttpRequestEvents：： OnResponseStart 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978011"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a><span data-ttu-id="6480c-103">IWinHttpRequestEvents：： OnResponseStart 事件</span><span class="sxs-lookup"><span data-stu-id="6480c-103">IWinHttpRequestEvents::OnResponseStart event</span></span>

<span data-ttu-id="6480c-104">開始接收回應資料時，就會發生 **OnResponseStart** 事件。</span><span class="sxs-lookup"><span data-stu-id="6480c-104">The **OnResponseStart** event occurs when the response data starts to be received.</span></span>

## <a name="syntax"></a><span data-ttu-id="6480c-105">語法</span><span class="sxs-lookup"><span data-stu-id="6480c-105">Syntax</span></span>


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a><span data-ttu-id="6480c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6480c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6480c-107">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6480c-107">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6480c-108">接收回應資料所傳回的標準狀態碼。</span><span class="sxs-lookup"><span data-stu-id="6480c-108">Receives the standard status code returned with the response data.</span></span> <span data-ttu-id="6480c-109">狀態碼定義于 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)中。</span><span class="sxs-lookup"><span data-stu-id="6480c-109">Status codes are defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="6480c-110">*ContentType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6480c-110">*ContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6480c-111">指定收到的內容類型，例如 "text/html" 或 "image/gif"。</span><span class="sxs-lookup"><span data-stu-id="6480c-111">Specifies the type of content received, such as "text/html" or "image/gif".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6480c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6480c-112">Return value</span></span>

<span data-ttu-id="6480c-113">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6480c-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6480c-114">備註</span><span class="sxs-lookup"><span data-stu-id="6480c-114">Remarks</span></span>

<span data-ttu-id="6480c-115">若要進行此事件，請使用 [ [**開啟**](iwinhttprequest-open.md) ] 以非同步模式傳送 HTTP 連接，然後使用 [ [**傳送**](iwinhttprequest-send.md) ] 將資料要求傳送到網際網路伺服器。</span><span class="sxs-lookup"><span data-stu-id="6480c-115">For this event to occur, use [**Open**](iwinhttprequest-open.md) to send an HTTP connection in asynchronous mode and use [**Send**](iwinhttprequest-send.md) to send a data request to an Internet server.</span></span>

<span data-ttu-id="6480c-116">這是在 [**傳送**](iwinhttprequest-send.md)之後第一個發生的 WinHTTP 事件。</span><span class="sxs-lookup"><span data-stu-id="6480c-116">This is the first WinHTTP event to occur after the [**Send**](iwinhttprequest-send.md).</span></span>

> [!Note]  
> <span data-ttu-id="6480c-117">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="6480c-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6480c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6480c-118">Requirements</span></span>



| <span data-ttu-id="6480c-119">需求</span><span class="sxs-lookup"><span data-stu-id="6480c-119">Requirement</span></span> | <span data-ttu-id="6480c-120">值</span><span class="sxs-lookup"><span data-stu-id="6480c-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6480c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6480c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6480c-122">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6480c-122">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="6480c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6480c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6480c-124">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="6480c-124">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="6480c-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6480c-125">Redistributable</span></span><br/>          | <span data-ttu-id="6480c-126">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6480c-126">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="6480c-127">Idl</span><span class="sxs-lookup"><span data-stu-id="6480c-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6480c-128"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6480c-128"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6480c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6480c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6480c-130">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="6480c-130">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="6480c-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="6480c-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="6480c-132">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="6480c-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




