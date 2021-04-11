---
title: " (Windows 網際網路) 快取"
description: WinINet 函數具有簡單但彈性的內建快取支援。
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093631"
---
# <a name="caching-windows-internet"></a> (Windows 網際網路) 快取

WinINet 函數具有簡單但彈性的內建快取支援。 從網路取出的任何資料都會快取在硬碟上，並針對後續的要求進行取出。 應用程式可以控制每個要求的快取。 若為來自伺服器的 HTTP 要求，也會快取大部分接收到的標頭。 從快取滿足 HTTP 要求時，快取的標頭也會傳回給呼叫端。 這可讓您順暢地下載資料，無論資料是來自快取或網路。

應用程式必須適當地配置緩衝區，才能在使用持續性 URL 快取函式時取得所需的結果。 如需詳細資訊，請參閱 [使用緩衝區](appendix-b-using-buffers.md)。

## <a name="cache-behavior-during-response-processing"></a>回應處理期間的快取行為

WinINet 快取符合 RFC 2616 中所述的 HTTP 快取控制指示詞。 快取控制指示詞和應用程式集旗標會決定可快取的內容;但是，WinINet 會根據下列準則來判斷實際快取的內容：

-   WinINet 只會快取 HTTP 和 FTP 回應。
-   快取只會儲存效能良好的回應，並在後續要求的回復中使用。 效能良好的回應會定義為成功傳回的回應。
-   根據預設，WinINet 會快取成功的回應，除非伺服器的快取控制指示詞，或應用程式定義的旗標明確表示回應可能不會被快取。
-   一般來說，如果符合上述需求，則會快取 GET 動詞命令的回應。 在任何情況下，都不會快取 PUT 和 POST 動詞命令的回應。
-   即使快取已滿，也會快取專案。 如果加入的專案會將快取置於大小限制，則會排程快取清除程式。 依預設，不保證專案在快取中保持超過10分鐘。 如需詳細資訊，請參閱 [下面的快](#cache-scavenger) 取清除程式一節。
-   預設會快取 Https。 這是由應用程式定義的快取指示詞無法覆寫的全域設定所管理。 若要覆寫全域設定，請在 [控制台] 中選取 [網際網路選項] 小程式，然後移至 [advanced] 索引標籤。核取 [安全性] 區段下的 [不要將加密的頁面儲存到磁片] 方塊。

## <a name="cache-scavenger"></a>快取清除

快取清除清理會定期從快取中清除專案。 如果將專案新增至快取，且快取已滿，則會將專案新增至快取，並排程快取清除程式。 如果快取清除程式完成一輪清除，而且快取尚未達到快取限制，則在另一個專案加入至快取時，會將清除程式排定為另一個四捨五入。 一般情況下，清除程式會在新增的專案將快取置於其大小限制時進行排程。 根據預設，快取中的最短存留時間會設定為10分鐘，除非在快取控制指示詞中另有指定。 快取清除程式啟動時，不保證最舊的專案是要從快取中刪除的第一個專案。

快取會在電腦上的所有 WinINet 應用程式中，針對相同的使用者共用。 從 Windows Vista 和 Windows Server 2008 開始，快取大小設定為 1/第32磁片的大小，最小大小為8MB，大小上限為50MB。

## <a name="using-flags-to-control-caching"></a>使用旗標來控制快取

快取旗標可讓應用程式控制其使用快取的時機和方式。 這些旗標可以單獨使用，也可以與存取網際網路上的資訊或資源的函式中的 *dwFlags* 參數一起使用。 根據預設，這些函式會儲存從網際網路下載的所有資料。

您可以使用下列旗標來控制快取。



| 值                                                                                                                                                  | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**網際網路旗標快取 \_ \_ \_ 非同步**](api-flags.md)                                                                            | 此旗標無效。                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_ \_ \_ \_ 網路 \_ 失敗時的網際網路旗標快取**](api-flags.md)                                                              | 如果資源的網路要求因 [ \_ 網際網路連線 \_ \_ 重設錯誤](wininet-errors.md) 或 [ \_ 網際網路 \_ 無法 \_ 連線](wininet-errors.md) 錯誤而失敗，則會從快取傳回資源。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)會使用此旗標。                                                                                                              |
| [**網際網路旗標不快取 \_ \_ \_**](api-flags.md)                                                                              | 不會快取資料，無論是在本機或任何閘道中。 與慣用值相同， [**網際網路 \_ 旗標 \_ 無 \_ \_**](api-flags.md)快取寫入。                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | 表示這是表單提交。                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**網際網路 \_\_ \_ 來自**](api-flags.md)快取 [**網際網路 \_ 旗標 \_ 表單 \_ 提交** 的旗標](api-flags.md) | 不會發出網路要求。 所有實體都會從快取傳回。 如果要求的專案不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不到錯誤檔案 \_ 。 只有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式會使用此旗標。                                                                                                                                                                                                       |
| [**網際網路 \_ 旗標 \_ FWD \_ 回**](api-flags.md)                                                                                  | 指出函式應使用目前在網際網路快取中的資源複本。 不會檢查資源的到期日和其他相關資訊。 如果在網際網路快取中找不到要求的專案，系統會嘗試找出網路上的資源。 此值是在 Microsoft Internet Explorer 5 中引進，並與 Internet Explorer 的 [ **向前** ] 和 [ **上一頁** ] 按鈕作業相關聯。 |
| [**網際網路 \_ 旗標 \_ 超連結**](api-flags.md)                                                                                 | 如果資源儲存在快取中，則會強制應用程式重載資源（如果沒有過期時間），而且不會傳回上次修改時間。                                                                                                                                                                                                                                                                                                                  |
| [**網際網路 \_ 旗標 \_ 設為 \_ 持續**](api-flags.md)                                                                    | 不再支援。                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**網際網路 \_ 旗標必須快取 \_ \_ \_ 要求**](api-flags.md)                                                             | 如果無法快取檔案，則會建立暫存檔案。 這與慣用的值相同，也就是 [**網際網路 \_ 旗標 \_ 需要 \_**](api-flags.md)的檔案。                                                                                                                                                                                                                                                                            |
| [**網際網路 \_ 旗標 \_ 需要檔案 \_**](api-flags.md)                                                                                | 如果無法快取檔案，則會建立暫存檔案。                                                                                                                                                                                                                                                                                                                                                                                               |
| [**網際網路 \_ 旗標無快取 \_ \_ \_ 寫入**](api-flags.md)                                                                     | 拒絕函數嘗試在快取中儲存從網際網路下載的資料。 如果應用程式不想將任何下載的資源儲存在本機，則需要此旗標。                                                                                                                                                                                                                                                               |
| [**網際網路 \_ 旗標 \_ 無 \_ UI**](api-flags.md)                                                                                        | 停用 cookie 對話方塊。 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)只可使用此旗標 (HTTP 要求) 。                                                                                                                                                                                                                                                                                          |
| [**網際網路 \_ 旗標 \_ 離線**](api-flags.md)                                                                                     | 防止應用程式將要求傳送至網路。 所有要求都是使用儲存在快取中的資源來解決。 如果資源不在快取中， \_ \_ 則會傳回適當的錯誤，例如找不 \_ 到錯誤檔案。                                                                                                                                                                                                                            |
| [**網際網路 \_ 旗標 \_ PRAGMA \_ NOCACHE**](api-flags.md)                                                                      | 強制源伺服器解析要求，即使 proxy 上有快取的複本也一樣。 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)函式只 (HTTP 和 HTTPS 要求) 且 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函式使用此旗標。                                                                                                                                                                                               |
| [**網際網路 \_ 旗標 \_ 重載**](api-flags.md)                                                                                       | 強制函式直接從網際網路取出要求的資源。 所下載的資訊會儲存在快取中。                                                                                                                                                                                                                                                                                                                     |
| [**網際網路 \_ 旗標重新 \_ 同步處理**](api-flags.md)                                                                         | 讓應用程式從網際網路執行資源的條件式下載。 如果儲存在快取中的版本是最新的，則會從快取下載資訊。 否則，就會從伺服器重載資訊。                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>持續性快取函數

需要持續性快取服務的用戶端會使用持續性快取功能，讓其應用程式將資料儲存在本機檔案系統中，以供後續使用，例如在低頻寬連結限制資料存取的情況下，或完全無法使用存取。

快取功能可提供持續性快取和離線流覽。 除非 [**網際網路 \_ 旗標 \_ 沒有 \_ \_**](api-flags.md) 明確指定快取的快取寫入旗標，否則函數會快取從網路下載的所有資料。 不會快取張貼資料的回應。

## <a name="using-the-persistent-url-cache-functions"></a>使用持續性 URL 快取函數

下列持續性 URL 快取功能可讓應用程式存取和操作儲存在快取中的資訊。



| 函式                                                           | 描述                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | 快取儲存體中指定檔案的資料，並將其與指定的 URL 產生關聯。                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | 快取儲存體中指定檔案的資料，並將其與指定的 URL 產生關聯。                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | 配置要求的快取儲存體，並建立本機檔案名以儲存對應于來源名稱的快取專案。                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | 產生快取群組識別。                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | 如果檔案存在，則從快取中移除與來源名稱相關聯的檔案。                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | 釋放在快取索引檔中的 **GROUPID** 和任何相關聯的狀態。                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | 關閉指定的列舉控制碼。                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | 開始快取的列舉。                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | 開始已篩選的快取列舉。                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | 抓取快取中的下一個專案。                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | 抓取已篩選快取列舉中的下一個專案。                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | 抓取快取專案的相關資訊。                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | 在轉譯任何會以離線模式套用的快取重新導向（ [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)）之後，搜尋 URL。           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | 從使用 [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)開啟的資料流程讀取快取的資料。                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | 從快取中，以檔案的形式抓取快取專案。                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | 提供最有效率、獨立執行的方式來存取快取資料。                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | 從快取群組新增或移除專案。                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | 設定網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構的指定成員。                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | 從 [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)抓取檔案時鎖定的快取專案解除鎖定，以供快取使用。 |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | 關閉使用 [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)取出的資料流程。                                           |



 

### <a name="enumerating-the-cache"></a>列舉快取

[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)和 [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)函數會列舉儲存在快取中的資訊。 [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) 會藉由採用搜尋模式、緩衝區和緩衝區大小來建立控制碼，並傳回第一個快取專案，來啟動列舉。 [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) 會採用 [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)、緩衝區和緩衝區大小所建立的控制碼，以傳回下一個快取專案。

這兩個函數都會將網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構儲存在緩衝區中。 此結構的大小會因每個專案而有所不同。 如果傳遞給其中一個函式的緩衝區大小不足，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤的 \_ \_ 緩衝區。 緩衝區大小變數包含取出該快取專案所需的緩衝區大小。 應配置緩衝區大小變數所表示之大小的緩衝區，並使用新的緩衝區再次呼叫該函式。

[**網際網路快 \_ 取 \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)結構包含結構大小、快取資訊的 URL、本機檔案名、快取專案類型、使用計數、命中率、大小、上次修改時間、到期日、上次存取、上次同步處理時間、標頭資訊、標頭資訊大小和副檔名。

[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)函式會採用搜尋模式、儲存網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)結構的緩衝區，以及緩衝區大小。 目前，只會執行預設搜尋模式，它會傳回所有快取專案。

列舉快取之後，應用程式應該呼叫 [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) 來關閉快取列舉控制碼。

下列範例會在清單方塊中顯示每個快取專案的 URL （ **IDC \_ CacheList**）。 它會使用最大快取 \_ \_ 專案 \_ 資訊 \_ 大小來初始配置緩衝區，因為較早版本的 WinINet API 不會正確地列舉快取。 較新的版本會正確地列舉快取，而且沒有快取大小的限制。 在具有 Internet Explorer 4.0 之 WinINet API 版本的電腦上執行的所有應用程式，都必須配置所需大小的緩衝區。 如需詳細資訊，請參閱 [使用緩衝區](appendix-b-using-buffers.md)。


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a>正在抓取快取專案資訊

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)函式可讓您針對指定的 URL 取得網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)結構。 此結構包含結構大小、快取資訊的 URL、本機檔案名、快取專案類型、使用計數、命中率、大小、上次修改時間、到期日、上次存取、上次同步處理時間、標頭資訊、標頭資訊大小和副檔名。

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) 接受 URL、網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構的緩衝區，以及緩衝區大小。 如果找到 URL，則會將資訊複製到緩衝區。 否則，函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ \_ \_ 找不到的錯誤檔案。 如果緩衝區大小不足以儲存快取專案資訊，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤的 \_ \_ 緩衝區不足。 取得資訊所需的大小會儲存在緩衝區大小變數中。

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) 不會進行任何 URL 剖析，因此在快取中找不到包含錨點 () 的 url \# ，即使資源已快取也是一樣。 例如，如果傳遞 URL " https://example.com/example.htm\#sample "，則函式會傳回錯誤檔案 \_ ， \_ \_ 即使 " https://example.com/example.htm " 在快取中也是一樣。

下列範例會針對指定的 URL 抓取快取專案資訊。 然後，此函式會在 **IDC \_ CacheDump** 編輯方塊中顯示標頭資訊。


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a>建立快取專案

應用程式會使用 [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) 和 [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) 函數來建立快取專案。

[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) 接受 URL、預期的檔案大小和副檔名。 然後，此函式會建立本機檔案名，以儲存對應至 URL 和副檔名的快取專案。

使用本機檔案名，將資料寫入本機檔案。 將資料寫入本機檔案之後，應用程式應該呼叫 [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)。

[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) 接受 URL、本機檔案名、到期日、上次修改時間、快取專案類型、標頭資訊、標頭資訊大小和副檔名。 然後，此函式會將資料快取在快取儲存體中指定的檔案中，並將其與指定的 URL 產生關聯。

下列範例會使用先前呼叫 [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)所建立的本機檔案名（儲存在 [ **\_ LocalFile**] 文字方塊中），在快取專案中儲存文字方塊中的文字（ **idc \_ CacheDump**）。 使用 **fopen**、 **fprintf** 和 **fclose** 將資料寫入檔案之後，會使用 [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)來認可該專案。


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a>刪除快取專案

[**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)函式會使用 URL 並移除與其相關聯的快取檔案。 如果快取檔案不存在，此函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會 \_ 傳回 \_ \_ 找不到的錯誤檔案。 如果快取檔案目前已鎖定或正在使用中，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ 拒絕存取錯誤 \_ 。 解除鎖定時，會刪除檔案。

### <a name="retrieving-cache-entry-files"></a>正在抓取快取專案檔

如果應用程式需要資源的檔案名，請使用 [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) 和 [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) 函數。 不需要檔案名的應用程式應該使用 [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)、 [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)和 [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) 函式來取得快取中的資訊。

[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) 不會進行任何 URL 剖析，因此在快取中找不到包含錨點 () 的 url \# ，即使資源已快取也是一樣。 例如，如果傳遞 URL " https://example.com/example.htm\#sample "，則函式會傳回錯誤檔案 \_ ， \_ \_ 即使 " https://example.com/example.htm " 在快取中也是一樣。

[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) 接受 URL、儲存網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構的緩衝區，以及緩衝區大小。 函式會針對呼叫端取得和鎖定。

使用檔案中的資訊之後，應用程式應該呼叫 [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) 來解除鎖定檔案。

### <a name="cache-groups"></a>快取群組

若要建立快取群組，必須呼叫 [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) 函數來產生快取群組的 **GROUPID** 。 您可以藉由提供快取專案的 URL 和網際網路快取 \_ \_ 群組，將旗標新增 \_ 至 [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) 函式，將專案新增至快取群組。 若要從群組中移除快取專案，請將快取專案的 URL 和 INTERNET \_ cache \_ group remove 旗標傳遞 \_ 給 [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)。

[**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)和 [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)函數可用來列舉指定之快取群組中的專案。 列舉完成之後，函式應該呼叫 [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)。

## <a name="handling-structures-with-variable-size-information"></a>處理具有變數大小資訊的結構

快取可包含每個儲存的 URL 的變數大小資訊。 這會反映在 [**網際網路快 \_ 取 \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 結構中。 當快取函式傳回此結構時，會建立一律為網際網路快取 [**\_ \_ 專案 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) 大小加上任何變數大小資訊的緩衝區。 如果指標成員不是 **Null**，它會指向緊接在結構後面的記憶體區域。 將函式所傳回的緩衝區複製到另一個緩衝區時，指標成員應固定為指向新緩衝區中的適當位置，如下列範例所示。

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

\_ \_ 如果您指定的緩衝區太小而無法包含函式所抓取的快取專案資訊，某些快取函數會失敗，並出現錯誤緩衝區錯誤訊息。 在此情況下，函式也會傳回所需的緩衝區大小。 然後，您可以配置適當大小的緩衝區，然後再次呼叫函式。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 
