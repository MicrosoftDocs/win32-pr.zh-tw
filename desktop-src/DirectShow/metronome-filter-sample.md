---
description: Metronome 篩選範例
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Metronome 篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea1b321dd2602829697862e2716c9017573a44b6162b355e78e586e14d85003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072982"
---
# <a name="metronome-filter-sample"></a>Metronome 篩選範例

## <a name="description"></a>描述

此範例篩選會顯示如何執行參考時鐘。 此篩選器會使用您的預設麥克風輸入來接聽音訊尖峰 (例如點擊、手拍手聲或咳嗽) ，以用來判斷時脈速率。

## <a name="usage"></a>使用方式

建立範例專案，並將篩選 DLL (Metronom.ax) 複製到您的 Windows 系統目錄。 執行 Metronom .reg 檔案以註冊 DLL。

若要使用篩選準則：

1.  在呈現影片資料流程的 GraphEdit 中建立篩選圖形。
2.  刪除任何呈現的音訊串流。
3.  將 Metronome 篩選器新增至圖形。 它會出現在 DirectShow 篩選準則分類中。
4.  執行圖形。 影片將會以正常速度開始播放。
5.  Clap 您的手，或使用 metronome 來設定新的速度。

## <a name="programming-notes"></a>程式設計附注

此篩選器只適用于影片。 音訊轉譯器無法同步處理至截然不同的頻率。

如果您每分鐘 clap 92 次 (每個 ~ 652 ms) 一次，則會以一般費率播放影片。 您可以變更 Metronom 中的常數值來變更這個預設值 `BPM` 。

如果您停止鼓掌一段時間，然後再重新開機鼓掌，您必須以大約相同的速度重新開機，否則篩選將會忽略它。 此外，影片播放速率會受限於 CPU 速度。 如果您超過任何時間長度的限制，篩選準則將會停止回應速率變更。 如果發生這種情況，請停止圖形並重新啟動。

如果您執行自己的時鐘，最重要的規則就是參考時鐘不能反向。 也就是說，它們絕對不能報告時間值小於前一個時間值。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的[Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ Metronome。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow樣品](directshow-samples.md)
</dt> </dl>

 

 



