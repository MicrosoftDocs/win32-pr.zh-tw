---
description: 檔案時間是64位的值，代表自上午12:00 以來經過的 100-毫微秒間隔數。 1601年1月1日國際標準時間 (UTC) 。 當應用程式建立、存取和寫入檔案時，系統會記錄檔案的時間。
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: 檔案時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5919a2378e08798e4cd64d8f8357cb55692bd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853104"
---
# <a name="file-times"></a>檔案時間

檔案 *時間* 是64位的值，代表自上午12:00 以來經過的 100-毫微秒間隔數。 1601年1月1日國際標準時間 (UTC) 。 當應用程式建立、存取和寫入檔案時，系統會記錄檔案的時間。

NTFS 檔案系統會以 UTC 格式儲存時間值，因此不會受到時區或日光節約時間變更的影響。 FAT 檔案系統會根據電腦的本機時間來儲存時間值。 例如，在華盛頓州儲存于3： 00 PST 的檔案會在 NTFS 磁片區上顯示為6： 00 EST，但在 FAT 磁片區上的紐約會顯示為3： 00 EST。

時間戳記會在不同的時間更新，並基於各種原因。 唯一的保證是，檔案時間戳記的保證是在變更的控制碼關閉時，檔案時間會正確地反映出來。

並非所有檔案系統都可以記錄建立和上次存取時間，而且並非所有檔案系統都會以相同的方式記錄它們。 例如，在 FAT 上的建立時間解析為10毫秒，而寫入時間的解析為2秒，而存取時間的解析為1天，所以實際上是存取日期。 NTFS 檔案系統會在最後一次存取後最多1小時延遲檔案的上次存取時間更新。

若要取得指定檔案的檔案時間，請使用 [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) 函數。 **GetFileTime** 會將建立、上次存取和上次寫入時間複製到個別的 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構。 您也可以使用 [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) 和 [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) 函數來取出檔案時間。 這些函數會將檔案時間複製到 [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa)結構中的 **FILETIME** 結構。 寫入檔案時，除非已關閉用於寫入的所有控制碼，否則最後寫入時間不會完全更新。

若要設定檔案的檔案時間，請使用 [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) 函數。 此函式可讓您修改建立、上次存取和上次寫入時間，而不需要變更檔案的內容。 您可以使用 [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) 函數來比較不同檔案的時間。 此函式會比較兩個檔案的時間，並傳回值，這個值會指出哪一個時間較晚，或傳回 0 (零) 如果時間相等。

如果您打算修改指定檔案的檔案時間，您可以使用 [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) 函式，將日期和時間轉換成檔案時間。 您也可以藉由呼叫 [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime)函數，以 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構取得系統時間。

若要讓使用者輕鬆地向使用者顯示檔案，請使用 [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) 函數。 **FileTimeToSystemTime** 會轉換檔案時間，並將月、日、年和日的時間從檔案時間複製到 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構。

## <a name="file-times-and-daylight-saving-time"></a>檔案時間和日光節約時間

如果使用者已將系統設定為自動調整日光節約時間，您必須小心使用檔案時間。

若要將檔案時間轉換為本地時間，請使用 [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) 函數。 不過， **FileTimeToLocalFileTime** 會使用時區和日光節約時間的目前設定。 因此，如果是日光節約時間，即使您要轉換的檔案時間是標準時間，也會將日光節約時間納入考慮。

FAT 檔案系統會以當地時間記錄磁片的時間。 [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) 會從 FAT 檔案系統抓取快取的 UTC 時間。 當它變成日光節約時間時， **GetFileTime** 所取出的時間會關閉一小時，因為快取未更新。 當您重新開機電腦時， **GetFileTime** 抓取的快取時間是正確的。 [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) 會從 FAT 檔案系統抓取當地時間，並使用時區和日光節約時間的目前設定，將其轉換為 UTC。 因此，如果是日光節約時間， **FindFirstFile** 會將日光節約時間納入考慮，即使您要轉換的檔案時間是標準時間也一樣。

NTFS 檔案系統會以 UTC 時間記錄磁片上的時間。 若要在將檔案時間轉換為當地時間時考慮日光節約時間，請使用下列一連串的函式，而不是使用 [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)：

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>檔案時間和 CDFS.SYS

使用 Compact 光碟檔案系統在媒體上的檔案日期和時間戳記 (CDFS.SYS) 會針對當地時區進行調整。 ISO 9660 指出，CDFS.SYS 是為了正確地顯示當地時區的日期資訊。 這樣做的目的是要讓 CDFS.SYS 上的檔案日期與國際磁碟格式的日期顯示 (UDF) 。 UDF 是發佈媒體的較新標準。 如果您的程式碼相依于使用 CDFS.SYS 從媒體或源自媒體的檔案未修改的日期資訊，則可能無法正確運作。

 

 
