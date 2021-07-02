---
description: 本主題將識別 WinHTTP 使用的常數。
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: WinHTTP 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113175002"
---
# <a name="winhttp-constants"></a><span data-ttu-id="06b5e-103">WinHTTP 常數</span><span class="sxs-lookup"><span data-stu-id="06b5e-103">WinHTTP Constants</span></span>

<span data-ttu-id="06b5e-104">WinHTTP 使用下列常數：</span><span class="sxs-lookup"><span data-stu-id="06b5e-104">WinHTTP uses the following constants:</span></span>

<dl>

<dt>

[<span data-ttu-id="06b5e-105">**錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="06b5e-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="06b5e-106">WinHTTP 函數特定的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="06b5e-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="06b5e-107">這些函數也會在適當的情況下傳回 Windows 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="06b5e-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="06b5e-108">對應至每個常數的值是應用程式開發介面的常數值， (API) 函式和 [**WinHttpRequest**](winhttprequest.md) 物件錯誤號碼的較低16位。</span><span class="sxs-lookup"><span data-stu-id="06b5e-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="06b5e-109">**HTTP 狀態碼**</span><span class="sxs-lookup"><span data-stu-id="06b5e-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="06b5e-110">常數和對應的值，指出網際網路上的伺服器所傳回的 HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="06b5e-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="06b5e-111">**選項旗標**</span><span class="sxs-lookup"><span data-stu-id="06b5e-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="06b5e-112">[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)和 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)支援的選項旗標。</span><span class="sxs-lookup"><span data-stu-id="06b5e-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="06b5e-113">所有有效的選項旗標值都大於或等於 WINHTTP \_ FIRST \_ 選項，且小於或等於 winHTTP \_ LAST \_ 選項。</span><span class="sxs-lookup"><span data-stu-id="06b5e-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="06b5e-114">**網際網路 \_ 埠**</span><span class="sxs-lookup"><span data-stu-id="06b5e-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="06b5e-115">指出埠的文字值。</span><span class="sxs-lookup"><span data-stu-id="06b5e-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="06b5e-116">**網際網路 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="06b5e-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="06b5e-117">WinHTTP 支援的網際網路架構。</span><span class="sxs-lookup"><span data-stu-id="06b5e-117">Internet schemes supported by WinHTTP.</span></span>

</dd>

<dt>

[<span data-ttu-id="06b5e-118">**查詢資訊旗標**</span><span class="sxs-lookup"><span data-stu-id="06b5e-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt>
<dd>

<span data-ttu-id="06b5e-119">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)所使用的屬性和修飾詞。</span><span class="sxs-lookup"><span data-stu-id="06b5e-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
</dd>

<dt>

<span data-ttu-id="06b5e-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span><span class="sxs-lookup"><span data-stu-id="06b5e-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span></span>
</dt>
<dd>

<span data-ttu-id="06b5e-121">的值為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="06b5e-121">Has a value of 0x00000001.</span></span> <span data-ttu-id="06b5e-122">表示 [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) 傳入的字串是 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="06b5e-122">Indicates to [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) that the strings passed in are Unicode strings.</span></span>
</dd>

<dt>

<span data-ttu-id="06b5e-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="06b5e-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span></span>
</dt>
<dd>

<span data-ttu-id="06b5e-124">的值為0x0000000000000001ull。</span><span class="sxs-lookup"><span data-stu-id="06b5e-124">Has a value of 0x0000000000000001ull.</span></span> <span data-ttu-id="06b5e-125">指示 [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) 在已填入提供的資料緩衝區或回應完成之前，不會完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="06b5e-125">Instructs [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) not to complete the call until the provided data buffer has been filled, or the response is complete.</span></span> <span data-ttu-id="06b5e-126">傳遞此旗標會使 **WinHttpReadDataEx** 的行為等同于 [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata)的行為。</span><span class="sxs-lookup"><span data-stu-id="06b5e-126">Passing this flag makes the behavior of **WinHttpReadDataEx** equivalent to that of [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span></span>
</dd>

</dl>
