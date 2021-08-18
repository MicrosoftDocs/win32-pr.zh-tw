---
description: StylusInput Api 可讓您與 tablet 畫筆資料串流互動。 若要與資料流程互動，請將 RealTimeStylus 物件新增至您的應用程式，並將外掛程式加入至 RealTimeStylus 物件。
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: StylusInput Api 的架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 961d6e3e94d47054afb28948685fce5fe1cafe9cbb0fa2f36e5a2d8508f28b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093154"
---
# <a name="architecture-of-the-stylusinput-apis"></a>StylusInput Api 的架構

StylusInput Api 可讓您與 tablet 畫筆資料串流互動。 若要與資料流程互動，請將 [**RealTimeStylus**](realtimestylus-class.md) 物件新增至您的應用程式，並將外掛程式加入至 **RealTimeStylus** 物件。

StylusInput Api 中提供兩個外掛程式。 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件會實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)介面。 **DynamicRenderer** 物件會在繪製時即時呈現筆墨。 [**GestureRecognizer**](gesturerecognizer-class.md)物件會實 **IStylusSyncPlugin** 和 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面。 **GestureRecognizer** 物件可識別應用程式手勢。

## <a name="definitions"></a>定義

描述 StylusInput Api 的章節中會使用下列詞彙：

同步外掛程式

實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 介面的類別。 同步外掛程式通常會直接由 [**RealTimeStylus**](realtimestylus-class.md) 物件呼叫。

非同步外掛程式

實 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的類別。 非同步外掛程式通常會在應用程式的使用者介面上呼叫 (UI) 執行緒。

同步外掛程式集合

[StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10))集合，這是[IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))物件的已排序集合。 同步外掛程式集合通常是指指派給[RealTimeStylus](/previous-versions/ms824830(v=msdn.10))物件之[SyncPluginCollection](/previous-versions/ms824833(v=msdn.10))屬性的集合。 只有同步外掛程式才能新增至同步的外掛程式集合。

非同步外掛程式集合

[StylusAsyncPluginCollection](/previous-versions/ms824808(v=msdn.10))集合，這是[IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))物件的已排序集合。 非同步外掛程式集合通常會參考指派給[RealTimeStylus](/previous-versions/ms824830(v=msdn.10))物件之[AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10))屬性的集合。 只有非同步外掛程式可以加入至非同步外掛程式集合。

## <a name="synchronous-and-asynchronous-plug-ins"></a>同步和非同步外掛程式

[**RealTimeStylus**](realtimestylus-class.md)物件是設計來提供從 tablet 畫筆即時存取資料流程的功能。 針對需要即時存取資料流程和 undemanding 的工作（例如封包篩選），建立或使用同步外掛程式。 針對不需要即時存取資料流程的工作建立或使用非同步外掛程式，例如在 [**InkDisp**](inkdisp-class.md) 物件中建立和儲存筆觸。

某些工作可能會需要大量運算，但需要即時存取資料流程，例如 multistroke 手勢辨識。 為了滿足這些需求，StylusInput Api 提供了串聯的 [**realtimestylus**](realtimestylus-class.md) 模型，可讓您使用兩個 **realtimestylus** 物件，每個都在自己的執行緒上執行。 如需有關串聯的 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。

如需使用和建立外掛程式的詳細資訊，請參閱使用 [StylusInput api](working-with-the-stylusinput-apis.md)。

## <a name="the-tablet-pen-data-stream"></a>Tablet 畫筆資料串流

[**RealTimeStylus**](realtimestylus-class.md)物件具有兩個包含 tablet 畫筆資料的內部佇列、輸入佇列和輸出佇列。 畫筆資料會轉換成 [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) 命名空間中的類別實例。 下列清單說明 **RealTimeStylus** 物件如何處理 tablet 畫筆資料：

[**RealTimeStylus**](realtimestylus-class.md)物件會先在其輸入佇列中，然後從 tablet 畫筆資料流程檢查外掛程式資料物件。

[**RealTimeStylus**](realtimestylus-class.md)物件會將一個外掛程式資料物件傳送到其同步外掛程式集合中的物件。 每個同步外掛程式都可以將資料新增至輸入或輸出佇列。

將外掛程式資料物件傳送到同步外掛程式集合的所有成員之後，會將外掛程式資料物件放在 [**RealTimeStylus**](realtimestylus-class.md) 物件的輸出佇列。

然後， [**RealTimeStylus**](realtimestylus-class.md) 物件會檢查下一個要處理的外掛程式資料物件。

當 [**realtimestylus**](realtimestylus-class.md) 物件的輸出佇列包含資料時， **realtimestylus** 物件會從其輸出佇列將一個外掛程式資料物件傳送到其非同步外掛程式集合中的物件。 每個非同步外掛程式都可以將資料加入至輸入或輸出佇列。 不過，由於非同步外掛程式是在 UI 執行緒上執行，因此會將資料加入至佇列，以與 **RealTimeStylus** 物件正在處理的目前畫筆資料相關，而不是與非同步外掛程式正在處理的資料相關。

下圖說明透過 [**RealTimeStylus**](realtimestylus-class.md) 物件和其外掛程式集合進行 tablet 畫筆資料的流程。

![透過 realtimestylus 物件和其外掛程式集合的 tablet 畫筆資料流程程](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

在此圖中，標示為 "A" 和 "B" 的圓形代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。 標示為 "C" 的圓形代表 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 它會傳送至同步的外掛程式集合，並放在輸出佇列中。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

如需有關如何將特定資料新增至佇列並加以處理的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。

## <a name="the-stylusinput-apis"></a>StylusInput Api

StylusInput Api 主要位於 [StylusInput](/previous-versions/ms824750(v=msdn.10)) 和 [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) 命名空間中。 不過，StylusInput Api 也會參考 [Microsoft Ink](/previous-versions/ms826516(v=msdn.10)) 命名空間中的某些類別，例如 [Tablet](/previous-versions/ms827783(v=msdn.10)) 類別、 [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) 集合，以及 [ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) 和 [SystemGesture](/previous-versions/ms827134(v=msdn.10)) 列舉。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))
</dt> <dt>

[**GestureRecognizer**](gesturerecognizer-class.md)
</dt> <dt>

[**RealTimeStylus**](realtimestylus-class.md)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[使用 StylusInput Api](working-with-the-stylusinput-apis.md)
</dt> <dt>

[串聯的 RealTimeStylus 模型](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
