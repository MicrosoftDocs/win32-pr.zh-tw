---
title: 正在抓取 HTTP 標頭
description: 本教學課程說明如何從 HTTP 要求中取出標頭資訊。
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9c1dbae3447d5ae44c8d348394f2dc802ed9d7b4af7d99fde19d0b5d2c3d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955508"
---
# <a name="retrieving-http-headers"></a>正在抓取 HTTP 標頭

本教學課程說明如何從 HTTP 要求中取出標頭資訊。

## <a name="implementation-steps"></a>執行步驟

有兩種方式可以取出標頭資訊：

-   使用與您的應用程式所需的 HTTP 標頭相關聯的其中一個 [**查詢資訊旗**](query-info-flags.md) 標常數。
-   使用 HTTP \_ 查詢 \_ 自訂屬性旗標，並傳遞 HTTP 標頭的名稱。

使用與您的應用程式所需的 HTTP 標頭相關聯的常數，在內部會更快，但可能會有 HTTP 標頭沒有相關聯的常數。 在這些情況下，可以使用 HTTP \_ 查詢 \_ 自訂屬性旗標的方法。

這兩種方法都使用 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 函數。 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 會採用發出 HTTP 要求的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼、一個屬性、一個緩衝區、一個包含緩衝區大小的 DWORD 值，以及一個索引值。 您也可以將修飾詞加入至傳遞給 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 的屬性，以指出應該傳回資料的格式。

### <a name="retrieving-headers-using-a-constant"></a>使用常數來抓取標頭

若要使用 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 函式來取得使用常數的 HTTP 標頭，請遵循下列步驟：

1.  從 [**屬性**](query-info-flags.md)清單中的常數呼叫 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 、 **Null** 緩衝區，以及保留緩衝區大小設定為零的變數。 此外，如果您的應用程式需要特定格式的資料，您可以從修飾 [**詞清單新增**](query-info-flags.md) 常數。
2.  如果要求的 HTTP 標頭存在，呼叫 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 應該會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 應該會 \_ 傳回錯誤 \_ 的緩衝區，而針對 *lpdwBufferLength* 參數傳遞的變數應該設定為所需的位元組數目。
3.  配置具有所需位元組數的緩衝區。
4.  請重試 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)的呼叫。

下列範例示範如何使用 HTTP [](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) \_ 查詢 \_ 原始 \_ 標頭 CRLF 常數來呼叫 HttpQueryInfo \_ ，這是一個特殊值，它會要求所有傳回的 HTTP 標頭。


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



### <a name="retrieving-headers-using-http_query_custom"></a>使用 HTTP \_ 查詢 \_ 自訂來抓取標頭

若要使用 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 函式來取得使用 HTTP 查詢自訂的 HTTP 標頭 \_ ，請遵循下列 \_ 步驟：

1.  配置夠大的緩衝區來保存 HTTP 標頭的字串名稱。
2.  將 HTTP 標頭的字串名稱寫入緩衝區。
3.  使用[](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) HTTP \_ 查詢 \_ 自訂、包含 HTTP 標頭字串名稱的緩衝區，以及保存緩衝區大小的變數來呼叫 HttpQueryInfo。 此外，如果您的應用程式需要特定格式的資料，您可以從修飾 [**詞清單新增**](query-info-flags.md) 常數。
4.  如果呼叫 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 失敗，且 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，請以所需的位元組數目重新配置緩衝區。
5.  將 HTTP 標頭的字串名稱再次寫入緩衝區。
6.  請重試 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)的呼叫。

下列範例示範如何使用 HTTP [](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) \_ 查詢 \_ 自訂常數來要求 content-type HTTP 標頭，以呼叫 HttpQueryInfo。


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
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 