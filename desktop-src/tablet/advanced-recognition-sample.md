---
description: Advanced 辨識範例示範 Microsoft Tablet PC Automation 應用程式開發介面的 advanced 功能， (API) 用於手寫辨識。
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Advanced 辨認範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e23a078ded9c6967f8e45780f8cb3a739b246f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689236"
---
# <a name="advanced-recognition-sample"></a>Advanced 辨認範例

Advanced 辨識範例示範 Microsoft Tablet PC Automation 應用程式開發介面的 advanced 功能， (API) 用於手寫辨識。

其中包含下列功能：

-   列舉已安裝的辨識器
-   使用特定語言建立辨識器內容
-   使用辨識器物件
-   設定辨識的智慧標籤和字組清單
-   使用指南改善辨識品質
-   動態背景識別
-   手勢辨識

使用的介面為： [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)、 **IInkRecoCoNtext**、 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)、 **IInkRecognitionGuide**、 **IInkWordList**、 [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)、 **IInkCollector**、 **IInkDisp**、 **IInkRenderer**、 **IInkDrawingAttributes**、 **IInkStrokes** 和 **IInkStroke**。

## <a name="ink-and-project-headers"></a>筆跡和專案標題

首先，請加入 Tablet PC 自動化介面的標頭。 這些會隨 Tablet PC Platform SDK 一起安裝。 TpcError 檔案包含 Tablet PC API 錯誤碼定義。


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



EventSinks .h 檔案會定義 **IInkEventsImpl** 和 **IInkRecognitionEventsImpl** 介面，並設定 [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md)、 [**筆劃**](inkcollector-stroke.md)和 [**手勢**](inkcollector-gesture.md) 事件。


```C++
#include "EventSinks.h"
```



ChildWnds 檔案包含 **CInkInputWnd** 和 **CRecoOutputWnd** 類別的定義，這些類別衍生自 ATL 的 CWindowImpl，並用於建立範例的子視窗。


```C++
#include "ChildWnds.h"
```



AdvReco 檔案會宣告 **CAdvRecoApp** 類別，這是此範例的應用程式視窗類別。


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>初始化應用程式視窗

視窗的 `Run` 方法會設定 **CAdvRecoApp** 物件、載入視窗的功能表和圖示、建立預設辨識器的 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件，以及啟動視窗的訊息迴圈。

視窗的 **>oncreate** 方法會處理 **WM \_ 建立** 事件並建立子視窗。 [**InkCollector**](inkcollector-class.md)物件會連接至筆墨收集器的事件來源，並啟用輸入視窗的筆墨輸入。 然後，它會建立 [**InkRecognizerGuide**](inkrecognizerguide-class.md) 物件，並使用筆墨收集 [**器的轉譯**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) 器屬性將辨識指南方塊矩形轉換成筆墨空間。 最後， **>oncreate** 方法會建立 [**InkWordList**](inkwordlist-class.md) 物件。

## <a name="handling-ink-collector-events"></a>處理筆墨收集器事件

視窗的 **OnStroke** 方法會處理筆墨收集器的 [**筆劃**](inkcollector-stroke.md) 事件。 新的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件會加入至筆墨收集器的 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)屬性 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))中。

視窗的 **OnGesture** 方法會處理筆墨收集器的 [**手勢**](inkcollector-gesture.md) 事件。 **OnGesture** 方法會先使用最高的信賴度手勢來識別手勢，並檢查視窗是否支援這個特定的手勢。 如果支援手勢，手勢的周框方塊會失效，因為手勢會從筆劃集合中移除。 如果不支援筆勢， **手勢** 事件會取消，而導致筆墨收集器引發 [**筆劃**](inkcollector-stroke.md) 事件。 最後，會更新結果視窗。

## <a name="handling-recognizer-context-events"></a>處理辨識器內容事件

視窗的 **OnRecognitionWithAlternates** 方法會處理辨識器內容的 [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) 事件。 **OnRecognitionWithAlternates** 方法會在 [結果] 視窗中顯示辨識結果。

## <a name="handling-menu-commands"></a>處理功能表命令

視窗的 **OnRecognizer** 方法會處理辨識器功能表上的命令。 如果選取了 **預設** 的命令，則會使用 [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85))的 [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer)方法來取出預設辨識器;否則，就會取出選取的辨識器。 然後會建立並使用辨識器內容，並更新功能表和狀態列。

視窗的 **OnFactoidWordlist** 方法會處理 **模擬** 功能表上的 [**使用單詞表**] 命令。 辨識器內容的 [ [**筆劃**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) ] 屬性會設定為 **Null** ，以重設辨識器內容。 如果已關閉 [**使用單詞表**] 選項，辨識器內容的 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)屬性會設定為 **Null**;否則，辨識器內容的 **單詞表** 屬性會設定為在 **>oncreate** 方法中建立的 [**InkWordList**](inkwordlist-class.md) 。 最後，筆墨收集器的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 會重新附加至辨識器內容，並呼叫辨識器內容的 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) 方法，並更新功能表。

視窗的 **OnFactoid** 方法會處理 **模擬** 功能表上的模擬命令。 它會先將辨識器內容的 [ [**筆劃**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) ] 屬性設定為 **Null**、將辨識器內容的 [ [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) ] 屬性設定為選取的模擬，然後將筆墨收集器的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 重新指派給辨識器內容。 如果辨識器內容支援 [模擬](factoid-constants.md) 物件，則會呼叫辨識器內容的 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) 方法;否則，就會顯示錯誤訊息。 最後，會更新功能表和狀態列。

視窗的 **OnGuide** 方法會處理 [ **節目表** ] 功能表上的命令。 如果辨識器內容支援節目表選項， **OnGuide** 方法會將辨識器內容的 [ [**筆劃**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) ] 屬性設定為 **Null**、將 [辨識器內容 [**指南**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) ] 屬性設定為 [選取的指南] 設定、將筆墨收集器的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 重新指派給辨識器內容，然後呼叫辨識器內容的 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) 方法。 否則，就會顯示錯誤訊息。 最後，會更新輸入視窗、功能表和狀態列。

視窗的 **OnMode** 方法會處理 **模式** 功能表上的命令。 它會停用筆墨收集器、更新筆墨收集器的 [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) 屬性、更新功能表，以及顯示或隱藏手勢清單。 最後，會啟用筆墨收集器。

視窗的 **OnRecognize** 方法會處理筆墨功能表上的 [ **辨識** ] 命令。 它會呼叫辨識器內容的 [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) 方法，以防止筆墨新增至辨識器內容。 這有時是必要的，因為並非所有辨識器都支援部分辨識。 然後，它會呼叫辨識器內容的 [**辨識**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) 方法，並將結果傳遞給視窗的 **OnRecognitionWithAlternates** 方法。 最後，筆墨收集器的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 會重新指派給辨識器內容。

視窗的 **OnClear** 方法會處理 [**筆跡**] 功能表上的 [**清除**] 命令。 它會從筆墨收集器的 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) 屬性刪除筆劃、釋出舊的筆觸集合，並為筆墨收集器的 **筆墨** 屬性建立新的筆劃集合，並將新的筆劃集合附加至辨識器內容。

視窗的 **OnExit** 方法會處理 **筆墨** 功能表上的 **EXIT** 命令，並引發 WM \_ CLOSE 事件。

## <a name="helper-methods"></a>Helper 方法

視窗的 **LoadMenu** 方法是從視窗的 **Run** 方法呼叫，並將支援的辨識器清單和支援的 factoids 清單新增至功能表中。 首先，它會抓取 [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85))。 然後，它會逐一查看可用的辨識器，並只選取在 [ **語言** ] 屬性中有語言清單的專案，這會新增至 [辨識 **器** ] 功能表。 最後，它會在 [ **模擬** ] 功能表中填入定義為全域常數的 factoids 清單。

當使用者選取新的辨識器時，會從視窗的 **OnRecognizer** 方法呼叫視窗的 **UseRecognizer** 方法。 它會建立辨識器內容、從辨識器事件接收器卸離舊的內容、清除和釋放舊的內容，並將新的內容附加至辨識器事件接收器。

然後， **UseRecognizer** 方法會檢查辨識器的 [**功能**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) 屬性，它會傳回 [**InkRecognizerCapabilities**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) 值。 如果辨識器支援線條輸入，則會啟用 [**節目表**] 功能表上的 [**線條**] 命令。 如果辨識器支援已裝箱的輸入，則會啟用 [ **方塊** ] 命令。 如果辨識器不支援可用的輸入，則會停用 [ **無** ] 命令。 如果不支援目前的節目表選取專案，則會更新辨識器內容和功能表的 [ [**節目表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) ] 屬性。

然後， **UseRecognizer** 方法會嘗試設定辨識器內容的 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) 和 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 屬性。 如果辨識器不支援其中一項設定，則會使用預設值，並更新功能表。

最後， **UseRecognizer** 方法會將筆墨收集器之 [**InkDisp**](inkdisp-class.md)物件的 [**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)屬性附加至辨識器內容、將輸出視窗的字型變更為辨識器的語言所支援的字型、重設輸出視窗，以及藉由呼叫辨識器內容的 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)方法來更新辨識結果。

視窗的 **GetGestureName** 方法是從視窗的 **OnGesture** 方法中呼叫。 它會搜尋手勢，並將索引傳回至手勢的名稱，該名稱會儲存在 AdvReco .rc 檔的字串資料表中。

 

 
