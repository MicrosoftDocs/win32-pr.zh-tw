---
description: " (API) 使用 StylusInput 應用程式設計介面時的執行緒考慮。"
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: StylusInput API 的執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f9a26da86295a322d926278eda87388c0105132eafd2dfa3d7a9f6c6655e48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819638"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>StylusInput API 的執行緒考慮

[**RealTimeStylus**](realtimestylus-class.md)物件是設計來提供從 tablet 畫筆即時存取資料流程的功能。 外掛程式，可將實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 或 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的物件加入至 **RealTimeStylus** 物件。 同步外掛程式通常會直接在高優先順序的執行緒上由 **RealTimeStylus** 物件呼叫，而非同步外掛程式通常會在應用程式的使用者介面上呼叫， (UI) 執行緒。 針對需要即時存取資料流程和 undemanding 的工作（例如封包篩選），建立或使用同步外掛程式。 針對不需要即時存取資料流程的工作建立或使用非同步外掛程式，例如筆墨收集。

因為 [**realtimestylus**](realtimestylus-class.md) 物件之非同步外掛程式集合的外掛程式資料已排入佇列，所以非同步外掛程式可能會在接收其 [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) 方法的呼叫之前接收資料，但在停用 **RealTimeStylus** 物件之後。 請注意，如果已停用 **realtimestylus** 物件，某些 **realtimestylus** 物件的方法和屬性會擲回例外狀況。

下列 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 介面方法可能會在 tablet 畫筆資料執行緒以外的執行緒上呼叫。

-   [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10))和 [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10))方法會線上程上呼叫，以更新 [**realtimestylus**](realtimestylus-class.md)物件的 [Enabled](/previous-versions/ms585380(v=vs.100))屬性，或在啟用 **realtimestylus** 物件時加入或移除外掛程式。
-   [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10))方法會在呼叫 [**RealTimeStylus**](realtimestylus-class.md)物件之 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10))方法的執行緒上呼叫。
-   [錯誤](/previous-versions/ms824754(v=msdn.10))方法是在同步外掛程式于擲回例外狀況時執行的執行緒上呼叫。

若要從同步外掛程式與您的應用程式互動，請使用 [**RealTimeStylus**](realtimestylus-class.md)物件的 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10))方法，並處理其中一個非同步外掛程式的自訂手寫筆資料。如果您從同步外掛程式對另一個執行緒進行同步呼叫，您可能會封鎖 **RealTimeStylus** 物件，因而封鎖筆墨收集。

某些工作可能需要對 tablet 畫筆的資料串流進行即時存取，例如 multistroke 手勢辨識。 StylusInput Api 提供了串聯的 [**realtimestylus**](realtimestylus-class.md) 模型，可讓您使用兩個 **RealTimeStylus** 物件，每個物件都會從不同的執行緒呼叫它的同步外掛程式。 如需有關串聯的 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。

> [!Note]  
> 您無法在不同的進程中將 [**RealTimeStylus**](realtimestylus-class.md) 物件附加至視窗或控制項。

 

如需 Tablet PC 一般執行緒考慮的詳細資訊，請參閱 [TABLET Pc 執行緒的考慮](tablet-pc-threading-considerations.md)

 

 
