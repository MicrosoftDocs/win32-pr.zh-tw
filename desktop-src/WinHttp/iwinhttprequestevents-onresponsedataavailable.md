---
description: 當資料可從回應中取得時，就會發生。
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: IWinHttpRequestEvents：： OnResponseDataAvailable 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988266"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a><span data-ttu-id="045e2-103">IWinHttpRequestEvents：： OnResponseDataAvailable 事件</span><span class="sxs-lookup"><span data-stu-id="045e2-103">IWinHttpRequestEvents::OnResponseDataAvailable event</span></span>

<span data-ttu-id="045e2-104">當資料可從回應中取得時，就會發生 **OnResponseDataAvailable** 事件。</span><span class="sxs-lookup"><span data-stu-id="045e2-104">The **OnResponseDataAvailable** event occurs when data is available from the response.</span></span>

## <a name="syntax"></a><span data-ttu-id="045e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="045e2-105">Syntax</span></span>


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a><span data-ttu-id="045e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="045e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="045e2-107">*資料* \[在\]</span><span class="sxs-lookup"><span data-stu-id="045e2-107">*Data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="045e2-108">以零為基底的位元組陣列，這個陣列會接收 Microsoft Windows HTTP 服務所收到的回應資料 (WinHTTP) 直到發生此事件為止。</span><span class="sxs-lookup"><span data-stu-id="045e2-108">A zero-based array of bytes that receives the response data received by Microsoft Windows HTTP Services (WinHTTP) up to the point that this event occurs.</span></span> <span data-ttu-id="045e2-109">這是 VT  \_ 陣列 \| Vt UI1 類型的變異 \_ 。</span><span class="sxs-lookup"><span data-stu-id="045e2-109">This is a **VARIANT** of type VT\_ARRAY \| VT\_UI1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="045e2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="045e2-110">Return value</span></span>

<span data-ttu-id="045e2-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="045e2-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="045e2-112">備註</span><span class="sxs-lookup"><span data-stu-id="045e2-112">Remarks</span></span>

<span data-ttu-id="045e2-113">因為資料是以位元組為單位，所以在放置於寬字元 (Unicode) 字串時，必須將其轉換成寬字元。</span><span class="sxs-lookup"><span data-stu-id="045e2-113">Because data is in bytes, it must be converted to wide characters when placed in a wide character (Unicode) string.</span></span>

> [!Note]  
> <span data-ttu-id="045e2-114">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="045e2-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="045e2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="045e2-115">Requirements</span></span>



| <span data-ttu-id="045e2-116">需求</span><span class="sxs-lookup"><span data-stu-id="045e2-116">Requirement</span></span> | <span data-ttu-id="045e2-117">值</span><span class="sxs-lookup"><span data-stu-id="045e2-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="045e2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="045e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="045e2-119">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="045e2-119">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="045e2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="045e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="045e2-121">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="045e2-121">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="045e2-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="045e2-122">Redistributable</span></span><br/>          | <span data-ttu-id="045e2-123">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="045e2-123">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="045e2-124">Idl</span><span class="sxs-lookup"><span data-stu-id="045e2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="045e2-125"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="045e2-125"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="045e2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="045e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045e2-127">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="045e2-127">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="045e2-128">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="045e2-128">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="045e2-129">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="045e2-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




