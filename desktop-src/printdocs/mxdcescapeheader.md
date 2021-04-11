---
description: MXDC \_ escape \_ HEADER \_ T 結構會保存使用 MXDC \_ ESCAPE 作為 nEscape 參數之 ExtEscape 呼叫的作業程式碼。 它也會提供輸入和輸出緩衝區的大小。
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: 'MXDC_ESCAPE_HEADER_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852412"
---
# <a name="mxdc_escape_header_t-structure"></a><span data-ttu-id="3f141-104">MXDC \_ ESCAPE \_ HEADER \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="3f141-104">MXDC\_ESCAPE\_HEADER\_T structure</span></span>

<span data-ttu-id="3f141-105">**MXDC \_ escape \_ HEADER \_ T** 結構會保存使用 [**MXDC \_ ESCAPE**](mxdc-escape.md)作為 *nEscape* 參數之 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)呼叫的作業程式碼。</span><span class="sxs-lookup"><span data-stu-id="3f141-105">The **MXDC\_ESCAPE\_HEADER\_T** structure holds the operation code for a call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with [**MXDC\_ESCAPE**](mxdc-escape.md) as the *nEscape* parameter.</span></span> <span data-ttu-id="3f141-106">它也會提供輸入和輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="3f141-106">It also provides the sizes of the input and output buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f141-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f141-107">Syntax</span></span>


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a><span data-ttu-id="3f141-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f141-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3f141-109">**cbInput**</span><span class="sxs-lookup"><span data-stu-id="3f141-109">**cbInput**</span></span>
</dt> <dd>

<span data-ttu-id="3f141-110">將傳遞給 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數之 *lpszOutData* 參數的輸入緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="3f141-110">The size of the input buffer that will be passed to the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="3f141-111">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="3f141-111">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="3f141-112">輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="3f141-112">The size of the output buffer.</span></span> <span data-ttu-id="3f141-113">這與 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *cbOutput* 參數值相同。</span><span class="sxs-lookup"><span data-stu-id="3f141-113">This is the same value as the *cbOutput* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="3f141-114">**opCode**</span><span class="sxs-lookup"><span data-stu-id="3f141-114">**opCode**</span></span>
</dt> <dd>

<span data-ttu-id="3f141-115">告訴 MXDC 要做什麼的程式碼常數。</span><span class="sxs-lookup"><span data-stu-id="3f141-115">The code constant that tells MXDC what to do.</span></span>



| <span data-ttu-id="3f141-116">作業碼</span><span class="sxs-lookup"><span data-stu-id="3f141-116">Operations code</span></span>                      | <span data-ttu-id="3f141-117">Description</span><span class="sxs-lookup"><span data-stu-id="3f141-117">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f141-118">MXDCOP \_ 取得 \_ 檔案名</span><span class="sxs-lookup"><span data-stu-id="3f141-118">MXDCOP\_GET\_FILENAME</span></span>                | <span data-ttu-id="3f141-119">在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszOutData* 參數中，傳回輸出檔案的完整路徑（以零終止的字串或該字串的大小）。</span><span class="sxs-lookup"><span data-stu-id="3f141-119">Returns, in the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function, either the full path of the output file as a zero-terminated string or the size of that string.</span></span> <span data-ttu-id="3f141-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="3f141-120">See Remarks.</span></span>                   |
| <span data-ttu-id="3f141-121">MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ</span><span class="sxs-lookup"><span data-stu-id="3f141-121">MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ</span></span> | <span data-ttu-id="3f141-122">將列印票證與 XPS 固定檔順序產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3f141-122">Associates a print ticket with an XPS fixed document sequence.</span></span>                                                                                                                                                         |
| <span data-ttu-id="3f141-123">MXDCOP \_ PRINTTICKET \_ 固定 \_ 檔</span><span class="sxs-lookup"><span data-stu-id="3f141-123">MXDCOP\_PRINTTICKET\_FIXED\_DOC</span></span>      | <span data-ttu-id="3f141-124">將列印票證與 XPS 檔產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3f141-124">Associates a print ticket with an XPS document.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="3f141-125">MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面</span><span class="sxs-lookup"><span data-stu-id="3f141-125">MXDCOP\_PRINTTICKET\_FIXED\_PAGE</span></span>     | <span data-ttu-id="3f141-126">將列印票證與 XPS 頁面產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3f141-126">Associates a print ticket with an XPS page.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="3f141-127">MXDCOP \_ SET \_ S0PAGE</span><span class="sxs-lookup"><span data-stu-id="3f141-127">MXDCOP\_SET\_S0PAGE</span></span>                  | <span data-ttu-id="3f141-128">將目前頁面的 XPS 標記傳送至輸出。</span><span class="sxs-lookup"><span data-stu-id="3f141-128">Sends the XPS markup of the current page to the output.</span></span>                                                                                                                                                                |
| <span data-ttu-id="3f141-129">MXDCOP \_ 設定 \_ S0PAGE \_ 資源</span><span class="sxs-lookup"><span data-stu-id="3f141-129">MXDCOP\_SET\_S0PAGE\_RESOURCE</span></span>        | <span data-ttu-id="3f141-130">將頁面上的資源（例如影像或字型）傳送至輸出。</span><span class="sxs-lookup"><span data-stu-id="3f141-130">Sends a resource on the page, such as an image or font, to the output.</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f141-131">MXDCOP \_ 設定 \_ XPSPASSTHRU \_ 模式</span><span class="sxs-lookup"><span data-stu-id="3f141-131">MXDCOP\_SET\_XPSPASSTHRU\_MODE</span></span>       | <span data-ttu-id="3f141-132">將 MXDC 置於傳遞狀態，讓應用程式可以直接將 XPS 寫入輸出檔，而不需要 MXDC 任何處理。</span><span class="sxs-lookup"><span data-stu-id="3f141-132">Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="3f141-133">您可以用這種方式撰寫整份檔或甚至是檔順序。</span><span class="sxs-lookup"><span data-stu-id="3f141-133">An entire document or even document sequence can be written in this way.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f141-134">備註</span><span class="sxs-lookup"><span data-stu-id="3f141-134">Remarks</span></span>

<span data-ttu-id="3f141-135">在呼叫 [**MXDC \_ escape**](mxdc-escape.md)之前， \_ 應用程式應該先使用 [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) ESCAPE 呼叫 [**EXTESCAPE**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)來確認驅動程式是否已 MXDC。</span><span class="sxs-lookup"><span data-stu-id="3f141-135">Before calling [**MXDC\_ESCAPE**](mxdc-escape.md),\_applications should first verify that the driver is MXDC by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="3f141-136">如果驅動程式是 MXDC，則函式會傳回以零結尾的字串 " http://schemas.microsoft.com/xps/2005/06 "。</span><span class="sxs-lookup"><span data-stu-id="3f141-136">If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".</span></span>

<span data-ttu-id="3f141-137">此結構一律是在其 *lpszInData* 參數中傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的資料開頭。</span><span class="sxs-lookup"><span data-stu-id="3f141-137">This structure is always at the beginning of the data passed to the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function in its *lpszInData* parameter.</span></span>

<span data-ttu-id="3f141-138">當 **opCode** 為 MXDCOP 時， \_ 取得 \_ 檔案名：</span><span class="sxs-lookup"><span data-stu-id="3f141-138">When **opCode** is MXDCOP\_GET\_FILENAME:</span></span>

-   <span data-ttu-id="3f141-139">[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數只包含 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構。</span><span class="sxs-lookup"><span data-stu-id="3f141-139">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="3f141-140">藉由呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 兩次來取得輸出檔案名。</span><span class="sxs-lookup"><span data-stu-id="3f141-140">Obtain the output filename by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) twice.</span></span>
    1.  <span data-ttu-id="3f141-141">第一次將4傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的 *cbOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="3f141-141">The first time, pass 4 to the *cbOutput* parameter of [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="3f141-142">將 *lpszOutData* 參數設定為指向任何已配置的4位元組記憶體。</span><span class="sxs-lookup"><span data-stu-id="3f141-142">Set the *lpszOutData* parameter to point to any allocated 4 bytes of memory.</span></span> <span data-ttu-id="3f141-143">完整檔案路徑的大小會在 **ExtEscape** 的 *lpszOutData* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="3f141-143">The size of the fully qualified file path will be returned in the *lpszOutData* parameter of **ExtEscape**.</span></span>
    2.  <span data-ttu-id="3f141-144">然後再呼叫一次函數。</span><span class="sxs-lookup"><span data-stu-id="3f141-144">Then call the function again.</span></span> <span data-ttu-id="3f141-145">這次將 *cbOutput* 和 *cbInput* 設定為 4 + *DataSize*。</span><span class="sxs-lookup"><span data-stu-id="3f141-145">This time set both *cbOutput* and *cbInput* to 4+ *DataSize*.</span></span> <span data-ttu-id="3f141-146">完整檔案路徑會在 [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) 結構中傳回。</span><span class="sxs-lookup"><span data-stu-id="3f141-146">The fully qualified file path will be returned in an [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) structure.</span></span>

<span data-ttu-id="3f141-147">當 **opCode** 為 MXDCOP \_ printticket \_ 固定 \_ 檔 \_ SEQ 或 MXDCOP 的 \_ printticket \_ 固定 \_ 檔時：</span><span class="sxs-lookup"><span data-stu-id="3f141-147">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ or MXDCOP\_PRINTTICKET\_FIXED\_DOC:</span></span>

-   <span data-ttu-id="3f141-148">[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)結構的 [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)結構所組成。</span><span class="sxs-lookup"><span data-stu-id="3f141-148">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="3f141-149">呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 和 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)的呼叫之間進行。</span><span class="sxs-lookup"><span data-stu-id="3f141-149">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="3f141-150">當 **opCode** 為 MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面：</span><span class="sxs-lookup"><span data-stu-id="3f141-150">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_PAGE:</span></span>

-   <span data-ttu-id="3f141-151">[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)結構的 [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)結構所組成。</span><span class="sxs-lookup"><span data-stu-id="3f141-151">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="3f141-152">對 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 的 [**呼叫與對**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="3f141-152">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="3f141-153">當 **opCode** 為 MXDCOP \_ SET \_ S0PAGE 時：</span><span class="sxs-lookup"><span data-stu-id="3f141-153">When **opCode** is MXDCOP\_SET\_S0PAGE:</span></span>

-   <span data-ttu-id="3f141-154">[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md)結構的 [**MxdcS0PageData**](mxdcs0pagedata.md)結構所組成。</span><span class="sxs-lookup"><span data-stu-id="3f141-154">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcS0PageData**](mxdcs0pagedata.md) structure concatenated into an [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) structure.</span></span>
-   <span data-ttu-id="3f141-155">對 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 的 [**呼叫與對**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="3f141-155">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>
-   <span data-ttu-id="3f141-156">呼叫應用程式負責驗證 XML。</span><span class="sxs-lookup"><span data-stu-id="3f141-156">The calling application is responsible for validating the XML.</span></span>
-   <span data-ttu-id="3f141-157">如果您在使用 MXDCOP set S0PAGE 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 時，將 MXDCOP \_ 設定 \_ S0PAGE \_ 資源作為頁面上每個資源的 **opCode** ， \_ 則串流耗用量會更有效率 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3f141-157">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="3f141-158">當 **opCode** 為 MXDCOP \_ SET \_ S0PAGE \_ RESOURCE：</span><span class="sxs-lookup"><span data-stu-id="3f141-158">When **opCode** is MXDCOP\_SET\_S0PAGE\_RESOURCE:</span></span>

-   <span data-ttu-id="3f141-159">[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數是由 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構和串連成 [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)結構的 [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md)結構所組成。</span><span class="sxs-lookup"><span data-stu-id="3f141-159">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) structure concatenated into an [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) structure.</span></span>
-   <span data-ttu-id="3f141-160">對 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 的 [**呼叫與對**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須進行呼叫，但在 **startpage** 和 **EndPage** 呼叫之間可能會有多個這類呼叫。</span><span class="sxs-lookup"><span data-stu-id="3f141-160">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), but there can be multiple such calls between the **StartPage** and **EndPage** calls.</span></span>
-   <span data-ttu-id="3f141-161">如果您在使用 MXDCOP set S0PAGE 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 時，將 MXDCOP \_ 設定 \_ S0PAGE \_ 資源作為頁面上每個資源的 **opCode** ， \_ 則串流耗用量會更有效率 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3f141-161">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="3f141-162">當 **opCode** 為 MXDCOP \_ SET \_ XPSPASSTHRU \_ 模式時：</span><span class="sxs-lookup"><span data-stu-id="3f141-162">When **opCode** is MXDCOP\_SET\_XPSPASSTHRU\_MODE:</span></span>

-   <span data-ttu-id="3f141-163">[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數只包含 **MXDC \_ ESCAPE \_ HEADER \_ T** 結構。</span><span class="sxs-lookup"><span data-stu-id="3f141-163">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="3f141-164">此呼叫必須在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)之前發生。</span><span class="sxs-lookup"><span data-stu-id="3f141-164">This call must occur before the call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f141-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f141-165">Requirements</span></span>



| <span data-ttu-id="3f141-166">需求</span><span class="sxs-lookup"><span data-stu-id="3f141-166">Requirement</span></span> | <span data-ttu-id="3f141-167">值</span><span class="sxs-lookup"><span data-stu-id="3f141-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3f141-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f141-168">Minimum supported client</span></span><br/> | <span data-ttu-id="3f141-169">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f141-169">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f141-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f141-170">Minimum supported server</span></span><br/> | <span data-ttu-id="3f141-171">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f141-171">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f141-172">標頭</span><span class="sxs-lookup"><span data-stu-id="3f141-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f141-173"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f141-173"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f141-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f141-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f141-175">列印</span><span class="sxs-lookup"><span data-stu-id="3f141-175">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3f141-176">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="3f141-176">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="3f141-177">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f141-177">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3f141-178">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="3f141-178">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="3f141-179">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="3f141-179">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

