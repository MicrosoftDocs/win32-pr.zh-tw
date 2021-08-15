---
title: Windows功能區架構開發人員指南
description: 本節所包含的主題將說明 Windows 功能區架構的特定層面。
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows功能區，架構
- 功能區，架構
- Windows功能區，開發人員指南
- 功能區，開發人員指南
- Windows 功能區的開發人員指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b30c5b2564dc918c6f9accfe5a5cb36a2d77222e3822a75a76332b1d3234cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850626"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Windows功能區架構開發人員指南

本節所包含的主題將說明 Windows 功能區架構的特定層面。

## <a name="basics"></a>基本概念

[建立功能區應用程式](windowsribbon-stepbystep.md)

若要讓 Windows 功能區架構使用功能區標記檔案，標記檔案必須編譯成二進位格式資源檔。 Microsoft Windows 軟體開發套件 (SDK)  (7.0 或更新版本的 (UICC) 包含專用的功能區標記編譯器，) 此用途。 除了編譯功能區標記的二進位版本之外，UICC 會產生 ID 定義標頭 ( .h) 檔案，該檔案會將所有標記專案公開至功能區主應用程式，以及在組建階段用來將影像和字串資源連結至主應用程式的資源 ( .rc) 檔。

[遷移至 Windows 功能區架構](ribbon-migration.md)

依賴傳統功能表、工具列和對話方塊的應用程式可以遷移至功能區架構命令系統 (UI) 的豐富、動態和內容驅動使用者介面。 這是將應用程式現代化和讓起死回生的簡單且有效的方式，同時也改善了其功能的協助工具、可用性及可探索性。

[瞭解命令和控制項](windowsribbon-commandscontrols.md)

將邏輯與展示分開的設計原理，就是激勵功能區架構的命令呈現系統的設計原理，也就是以設計模式為基礎的系統，其中的功能和行為會與公開這項功能的控制項分開執行。

## <a name="user-interface"></a>使用者介面

[指定功能區影像資源](windowsribbon-imageformats.md)

功能區架構是一種豐富的命令呈現系統，其設計目的是要在功能區使用者介面中廣泛地支援影像資源， (UI) 。 所有影像資源都是在 [功能區標記](windowsribbon-schema.md) 中宣告，或從功能區主機應用程式進行查詢。

針對 Windows 8 和更新版本，功能區架構支援下列圖形格式：32位 ARGB 點陣圖 (BMP) 檔和可移植網狀圖形 (PNG) 具有透明度的檔。

針對 Windows 7 及更早版本，影像資源必須符合 Windows 中所使用的標準 BMP 圖形格式。

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)

功能區命令列中裝載的控制項受限於功能區架構所強制執行的版面配置規則，並根據預設行為和版面配置範本的組合， (在功能區標記中宣告的架構定義和自訂) 。 這些規則會定義功能區架構的調適型配置行為，此行為會影響命令列中的控制項在執行時間如何適應各種功能區大小。

[使用資源庫](ribbon-controls-galleries.md)

功能區架構可為開發人員提供健全且一致的模型，以管理各種集合型控制項的動態內容。 藉由 (UI) 來調整並重新設定功能區使用者介面，這些動態控制項可讓架構在主應用程式和功能區本身中回應使用者互動，並提供彈性來處理各種執行時間環境。

[顯示內容索引標籤](ribbon-contextualtabs.md)

在功能區架構應用程式中，[內容] 索引標籤是一個隱藏的索引標籤控制項，會在應用程式工作區中的物件（例如影像）已選取或反白顯示時，顯示在索引標籤[列上。](windowsribbon-controls-tab.md)

[使用應用程式模式重新設定功能區](ribbon-applicationmodes.md)

功能區架構支援動態重新設定和公開功能區使用者介面的核心元素， (UI) 在執行時間，根據應用程式的狀態 (也稱為內容) 。 宣告並與標記中的特定元素相關聯時，應用程式支援的各種狀態稱為應用程式模式。

[自訂功能區色彩](ribbon-color.md)

功能區架構會公開一組色彩屬性，可讓應用程式在執行時間 (UI) 元素自訂各種功能區使用者介面的外觀。

[顯示功能區](ribbon-visibility.md)

功能區架構會公開一組屬性，可讓應用程式指定在執行時間顯示功能區使用者介面 (UI) 的方式。

## <a name="management"></a>管理

[保存功能區狀態](ribbon-statepersistence.md)

Windows Ribon framework (功能區) 提供在應用程式會話之間保留各種使用者設定和喜好設定狀態的功能。

[接聽功能區事件](listening-for-ribbon-events.md)

功能區架構使用[Windows (ETW) ](../etw/event-tracing-portal.md)基礎結構的事件追蹤，讓開發人員瞭解使用者如何與應用程式的功能區互動。

## <a name="markup-compiler"></a>標記編譯器

[編譯功能區標記](windowsribbon-intentcl.md)

若要讓功能區架構使用 [功能區標記](windowsribbon-schema.md) 檔案，必須將標記檔案編譯成二進位格式資源檔。 針對此用途，Microsoft Windows 軟體開發套件 (SDK)  (7.0 或更新版本) 中包含了專用標記編譯器（ (UICC) 的 UI 命令編譯器）。 除了編譯標記的二進位版本之外，UICC 會產生 ID 定義標頭 ( .h) 檔案，該檔案會將所有標記專案公開至功能區主應用程式，以及在組建階段用來將影像和字串資源連結至主應用程式的資源 ( .rc) 檔。

[瞭解標記編譯器訊息](windowsribbon-compilationerrors.md)

Windows 功能區架構 (功能區) 標記編譯器、UI 命令編譯器 (UICC.exe) ，會針對功能區架構和功能區架構所定義的一組額外規則驗證功能區標記。

 

 