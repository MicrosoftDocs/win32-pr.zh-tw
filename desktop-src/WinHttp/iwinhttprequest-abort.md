---
description: Abort 方法會中止 WinHTTP 傳送方法。
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: IWinHttpRequest：： Abort 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945028"
---
# <a name="iwinhttprequestabort-method"></a><span data-ttu-id="4696a-103">IWinHttpRequest：： Abort 方法</span><span class="sxs-lookup"><span data-stu-id="4696a-103">IWinHttpRequest::Abort method</span></span>

<span data-ttu-id="4696a-104">**Abort** 方法會中止 [WinHTTP](about-winhttp.md) [**傳送**](iwinhttprequest-send.md)方法。</span><span class="sxs-lookup"><span data-stu-id="4696a-104">The **Abort** method aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4696a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4696a-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="4696a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4696a-106">Parameters</span></span>

<span data-ttu-id="4696a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4696a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4696a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4696a-108">Return value</span></span>

<span data-ttu-id="4696a-109">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="4696a-109">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4696a-110">備註</span><span class="sxs-lookup"><span data-stu-id="4696a-110">Remarks</span></span>

<span data-ttu-id="4696a-111">您可以中止非同步和同步的 [**傳送**](iwinhttprequest-send.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4696a-111">You can abort both asynchronous and synchronous [**Send**](iwinhttprequest-send.md) methods.</span></span> <span data-ttu-id="4696a-112">若要中止同步 [**傳送**](iwinhttprequest-send.md)方法，您必須從 [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)事件內呼叫 **abort** 。</span><span class="sxs-lookup"><span data-stu-id="4696a-112">To abort a synchronous [**Send**](iwinhttprequest-send.md) method, you must call **Abort** from within an [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) event.</span></span>

> [!Note]  
> <span data-ttu-id="4696a-113">針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="4696a-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4696a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4696a-114">Requirements</span></span>



| <span data-ttu-id="4696a-115">需求</span><span class="sxs-lookup"><span data-stu-id="4696a-115">Requirement</span></span> | <span data-ttu-id="4696a-116">值</span><span class="sxs-lookup"><span data-stu-id="4696a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4696a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4696a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4696a-118">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4696a-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4696a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4696a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4696a-120">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="4696a-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4696a-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4696a-121">Redistributable</span></span><br/>          | <span data-ttu-id="4696a-122">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4696a-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4696a-123">Idl</span><span class="sxs-lookup"><span data-stu-id="4696a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4696a-124"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4696a-124"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4696a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4696a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4696a-126"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4696a-126"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4696a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4696a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4696a-128"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4696a-128"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4696a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4696a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4696a-130">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4696a-130">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4696a-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4696a-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4696a-132">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="4696a-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




