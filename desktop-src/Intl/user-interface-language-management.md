---
description: MUI 可讓您的應用程式以兩種方式管理使用者介面語言。
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: 消費者介面語言管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852fe20d3edb9795c2c2a9d3ec45c1e8ffe053ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386287"
---
# <a name="user-interface-language-management"></a>消費者介面語言管理

MUI 可讓您的應用程式以兩種方式管理使用者介面語言。 應用程式可以使用簡單的語言管理方法，方法是預設為作業系統語言設定。 或者，應用程式也可以支援自己的語言，讓使用者可以從中選取。 MUI API 也可讓您的應用程式直接存取作業系統所支援的語言和語言清單，並由資源載入器維護。 本主題的其餘部分定義系統支援的語言和語言回溯機制。

## <a name="languages-maintained-by-the-operating-system"></a>作業系統維護的語言

### <a name="system-default-ui-languageinstall-language"></a>系統預設 UI 語言/安裝語言

系統預設 UI 語言是用來設定 Windows 之當地語系化版本的語言。 除非使用者選取不同的語言，否則所有功能表、對話方塊、錯誤訊息和說明檔都會以這種語言表示。

在 Windows Vista 和更新版本上，系統預設的 UI 語言稱為「安裝語言」，並且扮演較有限的角色。 在大部分的情況下，它會由系統慣用的 UI 語言取代。 不過，在某些內容中，有一種一律已知完全支援的單一安裝語言會很有用。

沒有可設定系統預設 UI 語言的 MUI 函數。 若要取得此語言，應用程式可以呼叫 [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)。

### <a name="system-ui-language"></a>系統 UI 語言

作業系統將系統 UI 語言定義為使用者介面語言，可由系統管理員在主控台的 [地區及語言選項] 部分的 [ **Advanced** ] 索引標籤中設定。 如果目前的使用者尚未進行特定的語言設定，或是沒有使用中的帳戶登入，則作業系統會使用這種語言。 只有在電腦上安裝了一個以上的使用者介面語言時，才能變更語言。

> [!Note]  
> 您必須重新開機所有使用者和服務的作業系統，才能看到語言變更的效果。

 

沒有可設定系統 UI 語言的 MUI 函數。 若要取得此值，以 Windows Vista 和更新版本為目標的應用程式可以呼叫 [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) ，並取得系統慣用 UI 語言清單中的第一種語言。 以 Windows Vista 之前的作業系統為目標的應用程式無法使用 [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) ，而且應該根據系統 ui 語言永遠與系統預設 ui 語言相同的假設。

### <a name="user-ui-language"></a>使用者 UI 語言

使用者 UI 語言會決定用於功能表、對話方塊、說明檔等的使用者介面語言。 您可以在主控台的 [地區及語言選項] 部分的 [ **語言** ] 索引標籤中設定目前的使用者。 只有在電腦上安裝了一個以上的使用者介面語言時，才可以變更此語言。 請注意，使用者必須登出再重新登入，才會看到效果。 例如，跨國公司想要在其所有子公司中部署 Windows。 該公司會建立全域安裝作業，這會在所有用戶端上安裝英文版的 Windows，無論位置為何。 同時，它會根據電腦所屬的組織單位，安裝特定的語言模組。 當使用者第一次登入新安裝的作業系統時，Windows 會顯示為當地語系化版本。

在 Windows Vista 和更新版本中，使用者 UI 語言是使用者慣用 UI 語言清單中的第一種語言。 請注意，如果特定資源無法用於此語言，則可以使用回溯語言。

在 Windows Vista 之前的作業系統上，使用者 UI 語言通常與系統預設 UI 語言相同。 不過，對於 Windows MUI，這兩種語言可能會不同。

若要取得使用者 UI 語言，應用程式可以呼叫 [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) 或 [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)。 應用程式無法變更使用者 UI 語言，因為沒有可設定的函式。

## <a name="language-lists-maintained-by-the-operating-system"></a>作業系統維護的語言清單

### <a name="system-preferred-ui-languages-list"></a>系統慣用的 UI 語言清單

資源載入器會維護系統慣用的 UI 語言清單。 此清單中包含的語言是作業系統用於其本身資源的語言，例如功能表和對話方塊、訊息、INF 檔案和說明檔。 此清單是由系統預設 UI 語言和系統 UI 語言及其回退所組成。 應用程式可以藉由呼叫 [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)來取出系統慣用的 UI 語言。

### <a name="user-preferred-ui-languages-list"></a>使用者慣用的 UI 語言清單

資源載入器會使用使用者慣用的 UI 語言清單，其中包含使用者慣用的語言。 資源載入器會使用此清單中符合語言的資源（如果有的話），適用于特定的應用程式執行緒。 這些語言的優先順序高於任何系統喜好設定。 若要取得使用者慣用的 UI 語言，您的應用程式可以呼叫 [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)。

### <a name="process-preferred-ui-languages-list"></a>處理慣用的 UI 語言清單

在 Windows Vista 和更新版本上，資源載入器會維護一個處理常式慣用 UI 語言清單，其中包含由 MUI 應用程式執行中進程所設定的最多五個有效語言。 應用程式可以透過呼叫 [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)來設定語言。 應用程式可以藉由呼叫 [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages)來取得語言。

### <a name="thread-preferred-ui-languages-list"></a>執行緒慣用 UI 語言清單

在 Windows Vista 和更新版本上，資源載入器會使用執行緒慣用的 UI 語言清單，其中包含由 MUI 應用程式執行中進程中的執行緒所設定的最多五個有效語言。 這些語言可用於自訂應用程式使用者介面語言，並使其與作業系統語言不同。 執行緒慣用 UI 語言清單是以使用者慣用的 UI 語言、系統慣用 UI 語言和系統預設 UI 語言為基礎。

若要設定執行緒慣用 UI 語言，應用程式應該呼叫 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)。 為了取得這些語言，應用程式會呼叫 [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)。

## <a name="neutral-language-representation"></a>中性語言標記法

中性語言會以單獨的語言表示，不含區域或地區設定。 例如，英文 (加拿大) 語言（en-us）的中性標記法表示為 "en"。 雖然中性語言未與區域或地區設定相關聯，但您可以將它與資源集建立關聯。 一般而言，中性語言資源是以語言最普遍的區域中的使用為基礎。

如圖所示，假設您的 MUI 應用程式將德文版的德文語言資源當地語系化為德文 (瑞士) 表示為 de 和德文 (奧地利) 表示為 de，同時為德文 (德國) 建立一組完整的資源，並以 de 消除方式表示。 您必須考慮整個資源檔來決定此應用程式。 如果應用程式將取消刪除的資源複製為中性語言資源，則必須提供資源載入器的替代語言。 如果載入器找不到特定語言特定的資源檔，或取消輸入，則會切換回語言中立的「de」資源。 這些資源最可能比完全不同語言的資源更適合，例如，英文 (美國) ，也就是唯一可能的回退。

另一個範例是，應用程式可能完全不會當地語系化成貝里斯。 但是，支援英文 (貝里斯) 的語言喜好設定，以依表示，可讓應用程式回復為 "en" 資源。

## <a name="language-fallback-in-the-resource-loader"></a>資源載入器中的語言回退

Windows Vista 和更新版本會在資源載入器所使用的 preordered fallback 語言清單中排列使用者介面語言設定。 為了形成清單，作業系統結合了數種語言，如下所示：

-   執行緒慣用 UI 語言，由執行緒使用者介面語言和其中性形式組成。 範例為法國 (法國) 的 fr-fr，以及其中性形式 "fr" 和西班牙文 (西班牙) 和其中性形式 "es" 的 es。
-   處理慣用的 UI 語言，由進程使用者介面語言和其中性形式組成。 例如，德國 (德國) 和其中性形式「de」的解除刪除。
-   使用者 UI 語言及其中立形式。 例如，日本 (日本) 和其中性形式 "ja-jp" 的範例為 ja-jp。
-   系統 UI 語言和其中性形式。 例如，義大利文 (義大利) 及其中立形式「it」。
    > [!Note]  
    > 如果未設定使用者 UI 語言，此語言只會包含在回復清單中。

     

-   系統預設 UI 語言和其中性形式。 例如，西班牙文 (西班牙) 和其中性形式 "es" 的 es。

以下顯示合併的 fallback 清單。 請注意，語言的重複項（例如 es 和 es）已消除。 由於範例會將使用者 UI 語言設定為 ja-jp，因此系統 UI 語言不會出現在合併的回溯清單中。

fr-fr、fr、es、es、de de、de、ja-jp、ja

載入 MUI 應用程式的資源時，資源載入器會嘗試針對目前正在執行的應用程式執行緒，選取符合執行緒慣用 UI 語言清單的其中一個檔案。 如果資源載入器在所選語言與合併的回溯清單中的第一個語言特定資源之間找不到直接相符，它會檢查清單中的後續語言，直到找到可接受的回復。

如果資源載入器找不到需要的檔案，則必須使用「保證良好」的回復語言。 針對 MUI 資源技術，資源載入器會從所提供的資源設定資料判斷回溯語言。 如需詳細資訊，請參閱 [MUI 資源管理](mui-resource-management.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於多語系消費者介面](about-multilingual-user-interface.md)
</dt> <dt>

[地區設定和語言](locales-and-languages.md)
</dt> <dt>

[NLS 術語](nls-terminology.md)
</dt> </dl>

 

 



