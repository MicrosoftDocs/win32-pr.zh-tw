---
description: RealTimeStylus 類別可讓您從 tablet 畫筆與資料流程進行互動。 若要與資料流程互動，請將 RealTimeStylus 物件新增至您的應用程式，並將外掛程式加入至 RealTimeStylus 物件。
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: 使用 StylusInput Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676752f242aa428b583390d7c3d38c952b4c0edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970596"
---
# <a name="working-with-the-stylusinput-apis"></a>使用 StylusInput Api

[**RealTimeStylus**](realtimestylus-class.md)類別可讓您從 tablet 畫筆與資料流程進行互動。 若要與資料流程互動，請將 **RealTimeStylus** 物件新增至您的應用程式，並將外掛程式加入至 **RealTimeStylus** 物件。

外掛程式可以修改與空中封包、手寫筆向下、封包和手寫筆向上通知方法相關聯的資料。 外掛程式可以取消無線封包和封包通知方法。 外掛程式也可以將應用程式資料以 [CustomStylusData](/previous-versions/ms575208(v=vs.100)) 物件的形式新增至資料流程。 下列清單提供您可能想要使用或建立之常用外掛程式類別的概念。

-   篩選外掛程式：選擇性地移除或取消 tablet 畫筆資料流程中資料的物件。
-   修飾詞外掛程式：選擇性地修改 tablet 畫筆資料串流中資料的物件。
-   動態轉譯器外掛程式：此物件會即時顯示 tablet 畫筆資料，因為它正由 [**RealTimeStylus**](realtimestylus-class.md) 物件處理。 之後，如果是表單重新整理之類的事件，動態轉譯器外掛程式或筆跡集合外掛程式可能會重繪筆墨。
-   辨識器外掛程式：掃描 tablet 畫筆移動筆勢、手寫或其他字元的物件。
-   筆墨收集器外掛程式：來自 tablet 畫筆資料流程的物件會建立和儲存筆跡。
-   包裝函式外掛程式：一種外掛程式，可作為 [**RealTimeStylus**](realtimestylus-class.md) 物件與另一個外掛程式或物件之間的介面，以修改包裝物件的行為。

您可以建立動態轉譯器和筆墨集合外掛程式，以轉譯成各種內容，例如檔案、資料流程或顯示裝置。 筆墨也可以不同的格式儲存，例如 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件、嚴加防禦圖形交換格式 (GIF) 檔、筆跡序列化格式 (ISF) 檔或其他格式。

StylusInput Api 提供兩個外掛程式： [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 類別和 [**GestureRecognizer**](gesturerecognizer-class.md) 類別。 **DynamicRenderer** 類別會即時提供筆跡資料的基本轉譯，並且經過簡化，以對效能造成最大的影響。 **GestureRecognizer** 類別提供 [**RealTimeStylus**](realtimestylus-class.md)類別的手勢辨識。

## <a name="in-this-section"></a>本節內容

-   [使用 RealTimeStylus 類別](working-with-the-realtimestylus-class.md)
-   [外掛程式和 RealTimeStylus 類別](plug-ins-and-the-realtimestylus-class.md)
-   [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)
-   [StylusInput Api 的執行注意事項](implementation-notes-for-the-stylusinput-apis.md)
-   [筆墨-集合外掛程式](ink-collection-plug-ins.md)
-   [動態轉譯器外掛程式](dynamic-renderer-plug-ins.md)
-   [辨識器外掛程式](recognizer-plug-ins.md)

 

 
