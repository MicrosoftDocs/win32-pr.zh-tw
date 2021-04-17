---
description: DirectShow 應用程式程式設計簡介
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: DirectShow 應用程式程式設計簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6218a346a7eb9711259c025aef09133ef2e58f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385673"
---
# <a name="introduction-to-directshow-application-programming"></a>DirectShow 應用程式程式設計簡介

本文介紹 DirectShow 中使用的基本術語和概念。 閱讀本節之後，您就可以開始撰寫您的第一個 DirectShow 應用程式。

**篩選和篩選圖形**

DirectShow 的建立區塊是稱為 *篩選器* 的軟體元件。 篩選器是一種軟體元件，可在多媒體串流上執行某些作業。 例如，DirectShow 篩選器可以

-   讀取檔案
-   從影片捕獲裝置取得影片
-   解碼各種不同的串流格式，例如 MPEG-1 video
-   將資料傳遞至圖形或音效卡

篩選器會接收輸入並產生輸出。 例如，如果篩選器會解碼 MPEG-2 影片，則輸入為 MPEG 編碼的資料流程，而輸出是一系列未壓縮的影片框架。

在 DirectShow 中，應用程式會將篩選鏈連接在一起，以執行任何工作，讓某個篩選的輸出變成另一個篩選的輸入。 一組連接的篩選稱為 *篩選圖形*。 例如，下圖顯示用來播放 AVI 檔案的篩選圖形。

![用來播放 avi 檔案的篩選圖形](images/avi-filter-graph.png)

檔案來源篩選器會從硬碟讀取 AVI 檔。 AVI 分隔器篩選器會將檔案剖析成兩個數據流：壓縮的影片資料流程和音訊串流。 AVI 解壓縮程式篩選器會解碼影片畫面。 影片轉譯器篩選器會使用 DirectDraw 或 GDI 來繪製畫面上顯示的畫面格。 預設 DirectSound 裝置篩選器會使用 DirectSound 播放音訊串流。

應用程式不需要管理此資料流程。 相反地，篩選是由稱為「篩選圖形管理員」的高階元件所控制。 應用程式會進行高階 API 呼叫（例如「執行」 (以透過圖形移動資料) 或「停止」 (以停止) 資料的流程。 如果您需要更充分掌控資料流程作業，您可以直接透過 COM 介面存取篩選。 篩選圖形管理員也會將事件通知傳遞至應用程式。

篩選圖形管理員也提供另一個用途：它會透過將篩選連接在一起，提供應用程式建立篩選圖形的方法。  (DirectShow 也提供可簡化此程式的各種 helper 物件。 這些會在檔中完整說明。 ) 

**撰寫 DirectShow 應用程式**

大致上，有三個可供任何 DirectShow 應用程式執行的工作。 如下圖所示。

![典型的 directshow 應用程式](images/fgm.png)

1.  應用程式會建立篩選圖形管理員的實例。
2.  應用程式會使用篩選圖形管理員來建立篩選圖形。 圖形中的一組確切篩選器將視應用程式而定。
3.  應用程式會使用篩選圖形管理員來控制篩選圖形，並透過篩選來串流資料。 在整個過程中，應用程式也會回應篩選圖形管理員的事件。

處理完成時，應用程式會釋放篩選圖形管理員和所有篩選。

DirectShow 是以 COM 為基礎;篩選圖形管理員和篩選器都是 COM 物件。 開始程式設計 DirectShow 之前，您應該先對 COM 用戶端程式設計有大致的瞭解。 有許多關於 COM 程式設計的書籍都可供使用。

若要開始使用 DirectShow，請閱讀文章 [如何播放](how-to-play-a-file.md)檔案，該檔案提供簡單的主控台應用程式來播放影片檔案。 [關於 directshow](about-directshow.md)的章節會更詳細地說明 directshow 架構，而[使用 directshow](using-directshow.md)的區段會檢查 directshow 所支援的主要案例，例如捕捉、影片編輯、DVD 播放和電視。

 

 



