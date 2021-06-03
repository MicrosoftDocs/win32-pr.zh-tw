---
description: Unicode (ICU) 的國際元件是一組成熟、廣泛使用的開放原始碼全球化 Api。
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Unicode 的國際元件 (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560a2f344a3024685e17df0f434f8ffa040b5c8b
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349987"
---
# <a name="international-components-for-unicode-icu"></a>Unicode 的國際元件 (ICU)

Unicode (ICU) 的國際元件是一組成熟、廣泛使用的開放原始碼全球化 Api。 ICU 利用 Unicode 的廣泛通用地區設定資料存放庫 (CLDR) 作為其資料庫，提供軟體應用程式的全球化支援。 ICU 具有廣泛的可攜性，讓應用程式在所有平臺上都有相同的結果。

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>ICU 所提供全球化 API 服務的重點

-   **字碼頁轉換**：將文字資料轉換成 Unicode 和幾乎任何其他字元集或編碼。 在數十年的過程中，ICU 的轉換資料表是以 IBM 收集的字元集資料為基礎，而且是最完整的可用位置。
-   定 **序**：根據特定語言、區域或國家/地區的慣例和標準來比較字串。 ICU 的定序是以 Unicode 定序演算法和 CLDR 的地區設定專屬比較規則為基礎。
-   **格式**：根據所選地區設定的慣例來格式化數位、日期、時間和貨幣數量。 這包括將月份和日名稱轉譯為選取的語言、選擇適當的縮寫、正確地排序欄位等等。這種資料也來自一般地區設定資料存放庫。
-   **時間計算**：提供多種類型的行事曆給傳統西曆以外的時間。 提供一組完整的時區計算 Api。
-   **Unicode 支援**： ICU 緊密地追蹤 unicode 標準，可讓您輕鬆存取所有的 unicode 字元屬性、unicode 正規化、案例折迭，以及 [unicode 標準](https://www.unicode.org/)所指定的其他基本作業。
-   **正則運算式**： ICU 的正則運算式完全支援 Unicode，同時提供極具競爭力的效能。
-   **雙向**：支援處理包含由左到右混合的文字 (英文) ，以及由右至左 (阿拉伯文或希伯來文) 資料。

如需詳細資訊，您可以造訪 ICU 網站： <http://site.icu-project.org/>

## <a name="overview"></a>概觀

在 Windows 10 Creators Update 中，ICU 已整合至 Windows，讓 C Api 和資料可供公開存取。

> [!IMPORTANT]
> Windows 中的 ICU 版本只會公開 C Api。 它不會公開任何 c + + Api。 可惜的是，因為 c + + 缺乏穩定的 ABI，所以無法公開 c + + Api。

如需有關 ICU C Api 的檔，請參閱這裡的官方 ICU 檔頁面： <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Windows 中 ICU 文件庫的變更歷程記錄

### <a name="version-1703-creators-update"></a>版本 1703 (建立者更新) 
在此版本中，會先將 ICU 程式庫新增至 Windows 10 作業系統。
它已新增為：
- 兩個系統 Dll：
    -   **icuuc.dll** (這是 ICU 的「一般」程式庫) 
    -   **icuin.dll** (這是 ICU 「國際化」程式庫) 
- Windows 10 SDK 中有兩個標頭檔：
    -   **icucommon。h**
    -   **icui18n。h**
- Windows 10 SDK 中有兩個匯入程式庫：
    -   **icuuc .lib**
    -   **icuin .lib**

### <a name="version-1709-fall-creators-update"></a>版本 1709 (秋季建立者更新) 
已加入合併的標頭檔（ **icu. h**），其中包含上述兩個標頭檔的內容 (icucommon 和 icui18n) ，而且也會將的型別變更 `UCHAR` 為 `char16_t` 。

### <a name="version-1903-may-2019-update"></a>1903版 (2019 更新) 
已加入新的組合 DLL **icu.dll**，其中包含 "common" 和 "國際化" 程式庫。 此外，已將新的匯入程式庫新增至 Windows 10 SDK： **icu.**.。

接下來，將不會在舊的標頭中加入新的 Api (icucommon .h 和 icui18n) 或舊的匯入程式庫 (icuuc .lib 和 icuin .lib) 。 新的 Api 只會加入至合併的標頭 (icu. h) 和合併的匯入程式庫 (icu...... a) 。

## <a name="getting-started"></a>開始使用

需要遵循三個主要步驟： (Windows 10 Creators Update 或更高版本) 

<dl>

1. 您的應用程式必須以 Windows 10 1703 版 (建立者更新) 或更高版本為目標。

2. 加入標頭：

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   在 Windows 10 1709 版和更新版本上，您應該改為包含合併的標頭：

   ``` syntax
   #include <icu.h>
   ```
  
3. 連結至這兩個程式庫：

   -   icuuc .lib
   -   icuin .lib

   在 Windows 10 1903 版和更新版本上，您應該改用組合的程式庫：

   -   icu. .lib

</dl>

然後，您可以從您想要的這些程式庫呼叫任何 ICU C API。  (不會公開任何 c + + Api。 ) 

> [!IMPORTANT]
> 如果您使用舊版的匯入程式庫（icuuc .lib 和 icuin），請確定它們列在 [其他相依性連結器] 設定中的 [] 程式庫之前（例如 onecoreuap .lib 或 >windowsapp）， (查看下圖) 。 否則，連結器會連結至 icu，這會導致在執行時間嘗試載入 icu.dll。 只有從1903版開始才會出現該 DLL。 因此，如果使用者在1903版的 Windows 電腦上升級 Windows 10 SDK，應用程式將無法載入並執行。 如需 Windows 中 ICU 文件庫的歷程記錄，請參閱 [windows 中 icu 文件庫的變更歷程記錄](#history-of-changes-to-the-icu-library-in-windows)。

![icu 範例](images/icu-example.png)

> [!Note]  
>
> - 這是 [所有平臺] 的設定。
> - 針對要使用 ICU 的 Win32 應用程式，他們必須先呼叫 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 。 在 Windows 10 1903 版和更新版本上，可以使用合併的 ICU 程式庫 (icu.dll/icu.lib) ，您可以使用合併的程式庫省略 CoInitializeEx 呼叫。
> - 並非 ICU Api 所傳回的所有資料都會與 Windows 作業系統一致，因為此對齊工作仍在進行中。 

## <a name="icu-example-app"></a>ICU 範例應用程式

### <a name="example-code-snippet"></a>範例程式碼片段

以下範例說明如何在 c + + UWP 應用程式中使用 ICU Api。  (它不是完整的獨立應用程式，而只是呼叫 ICU 方法的範例。 ) 

下列小型範例假設有方法 **ErrorMessage** 和 **OutputMessage** 會以某種方式將字串輸出至使用者。

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



