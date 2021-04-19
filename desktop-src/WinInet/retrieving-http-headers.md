---
title: 正在抓取 HTTP 標頭
description: 本教學課程說明如何從 HTTP 要求中取出標頭資訊。
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b31043940b8c2127d1cfa1696d2821641d0784
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969923"
---
# <a name="retrieving-http-headers"></a><span data-ttu-id="3df06-103">正在抓取 HTTP 標頭</span><span class="sxs-lookup"><span data-stu-id="3df06-103">Retrieving HTTP Headers</span></span>

<span data-ttu-id="3df06-104">本教學課程說明如何從 HTTP 要求中取出標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="3df06-104">This tutorial describes how to retrieve header information from HTTP requests.</span></span>

## <a name="implementation-steps"></a><span data-ttu-id="3df06-105">執行步驟</span><span class="sxs-lookup"><span data-stu-id="3df06-105">Implementation Steps</span></span>

<span data-ttu-id="3df06-106">有兩種方式可以取出標頭資訊：</span><span class="sxs-lookup"><span data-stu-id="3df06-106">There are two ways to retrieve the header information:</span></span>

-   <span data-ttu-id="3df06-107">使用與您的應用程式所需的 HTTP 標頭相關聯的其中一個 [**查詢資訊旗**](query-info-flags.md) 標常數。</span><span class="sxs-lookup"><span data-stu-id="3df06-107">Use one of the [**Query Info Flag**](query-info-flags.md) constants associated with the HTTP header that your application needs.</span></span>
-   <span data-ttu-id="3df06-108">使用 HTTP \_ 查詢 \_ 自訂屬性旗標，並傳遞 HTTP 標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="3df06-108">Use the HTTP\_QUERY\_CUSTOM attribute flag and pass the name of the HTTP header.</span></span>

<span data-ttu-id="3df06-109">使用與您的應用程式所需的 HTTP 標頭相關聯的常數，在內部會更快，但可能會有 HTTP 標頭沒有相關聯的常數。</span><span class="sxs-lookup"><span data-stu-id="3df06-109">Using the constant associated with the HTTP header that your application needs is faster internally, but there might be HTTP headers that do not have a constant associated with them.</span></span> <span data-ttu-id="3df06-110">在這些情況下，可以使用 HTTP \_ 查詢 \_ 自訂屬性旗標的方法。</span><span class="sxs-lookup"><span data-stu-id="3df06-110">For those cases, the method using the HTTP\_QUERY\_CUSTOM attribute flag is available.</span></span>

<span data-ttu-id="3df06-111">這兩種方法都使用 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 函數。</span><span class="sxs-lookup"><span data-stu-id="3df06-111">Both methods use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function.</span></span> <span data-ttu-id="3df06-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 會採用發出 HTTP 要求的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼、一個屬性、一個緩衝區、一個包含緩衝區大小的 DWORD 值，以及一個索引值。</span><span class="sxs-lookup"><span data-stu-id="3df06-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle on which the HTTP request was made, one attribute, a buffer, a DWORD value that contains the buffer size, and an index value.</span></span> <span data-ttu-id="3df06-113">您也可以將修飾詞加入至傳遞給 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 的屬性，以指出應該傳回資料的格式。</span><span class="sxs-lookup"><span data-stu-id="3df06-113">A modifier can also be added to the attribute passed to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to indicate in what format the data should be returned.</span></span>

### <a name="retrieving-headers-using-a-constant"></a><span data-ttu-id="3df06-114">使用常數來抓取標頭</span><span class="sxs-lookup"><span data-stu-id="3df06-114">Retrieving Headers Using a Constant</span></span>

<span data-ttu-id="3df06-115">若要使用 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 函式來取得使用常數的 HTTP 標頭，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="3df06-115">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using a constant, follow these steps:</span></span>

1.  <span data-ttu-id="3df06-116">從 [**屬性**](query-info-flags.md)清單中的常數呼叫 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 、 **Null** 緩衝區，以及保留緩衝區大小設定為零的變數。</span><span class="sxs-lookup"><span data-stu-id="3df06-116">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with a constant from the [**Attributes**](query-info-flags.md) list, a **NULL** buffer, and the variable that holds the buffer size set to zero.</span></span> <span data-ttu-id="3df06-117">此外，如果您的應用程式需要特定格式的資料，您可以從修飾 [**詞清單新增**](query-info-flags.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="3df06-117">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
2.  <span data-ttu-id="3df06-118">如果要求的 HTTP 標頭存在，呼叫 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 應該會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 應該會 \_ 傳回錯誤 \_ 的緩衝區，而針對 *lpdwBufferLength* 參數傳遞的變數應該設定為所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3df06-118">If the requested HTTP header exists, the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) should fail, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should return ERROR\_INSUFFICIENT\_BUFFER, and the variable passed for the *lpdwBufferLength* parameter should be set to the number of bytes required.</span></span>
3.  <span data-ttu-id="3df06-119">配置具有所需位元組數的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3df06-119">Allocate a buffer with the number of bytes required.</span></span>
4.  <span data-ttu-id="3df06-120">請重試 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3df06-120">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="3df06-121">下列範例示範如何使用 HTTP [](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) \_ 查詢 \_ 原始 \_ 標頭 CRLF 常數來呼叫 HttpQueryInfo \_ ，這是一個特殊值，它會要求所有傳回的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="3df06-121">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_RAW\_HEADERS\_CRLF constant, which is a special value that requests all of the returned HTTP headers.</span></span>


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a><span data-ttu-id="3df06-122">使用 HTTP \_ 查詢 \_ 自訂來抓取標頭</span><span class="sxs-lookup"><span data-stu-id="3df06-122">Retrieving Headers Using HTTP\_QUERY\_CUSTOM</span></span>

<span data-ttu-id="3df06-123">若要使用 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 函式來取得使用 HTTP 查詢自訂的 HTTP 標頭 \_ ，請遵循下列 \_ 步驟：</span><span class="sxs-lookup"><span data-stu-id="3df06-123">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using HTTP\_QUERY\_CUSTOM, follow these steps:</span></span>

1.  <span data-ttu-id="3df06-124">配置夠大的緩衝區來保存 HTTP 標頭的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="3df06-124">Allocate a buffer that is large enough to hold the string name of the HTTP header.</span></span>
2.  <span data-ttu-id="3df06-125">將 HTTP 標頭的字串名稱寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3df06-125">Write the string name of the HTTP header into the buffer.</span></span>
3.  <span data-ttu-id="3df06-126">使用[](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) HTTP \_ 查詢 \_ 自訂、包含 HTTP 標頭字串名稱的緩衝區，以及保存緩衝區大小的變數來呼叫 HttpQueryInfo。</span><span class="sxs-lookup"><span data-stu-id="3df06-126">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with HTTP\_QUERY\_CUSTOM, the buffer that contains the string name of the HTTP header, and the variable that holds the buffer size.</span></span> <span data-ttu-id="3df06-127">此外，如果您的應用程式需要特定格式的資料，您可以從修飾 [**詞清單新增**](query-info-flags.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="3df06-127">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
4.  <span data-ttu-id="3df06-128">如果呼叫 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 失敗，且 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，請以所需的位元組數目重新配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3df06-128">If the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, reallocate a buffer with the number of bytes required.</span></span>
5.  <span data-ttu-id="3df06-129">將 HTTP 標頭的字串名稱再次寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3df06-129">Write the string name of the HTTP header into the buffer again.</span></span>
6.  <span data-ttu-id="3df06-130">請重試 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3df06-130">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="3df06-131">下列範例示範如何使用 HTTP [](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) \_ 查詢 \_ 自訂常數來要求 content-type HTTP 標頭，以呼叫 HttpQueryInfo。</span><span class="sxs-lookup"><span data-stu-id="3df06-131">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_CUSTOM constant to request the Content-Type HTTP header.</span></span>


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="3df06-132">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="3df06-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="3df06-133">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="3df06-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="3df06-134">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="3df06-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 