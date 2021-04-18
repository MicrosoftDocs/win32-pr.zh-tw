---
title: Windows 動畫詞彙
description: 本詞彙包含使用 Windows 動畫管理員之開發人員感興趣的詞彙和縮寫。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Windows 動畫 Windows 動畫，詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2019
ms.locfileid: "104507761"
---
# <a name="windows-animation-glossary"></a>Windows 動畫詞彙

本詞彙包含使用 Windows 動畫管理員之開發人員感興趣的詞彙和縮寫。

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**動畫** 
</dt> <dd>

一系列的綜合、連續的靜止影像，會在播放時產生移動的假像。

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**動畫管理員** 
</dt> <dd>

Windows 動畫的核心元件和中央程式設計介面，可用於管理 (建立、排程及控制) 的動畫。

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**動畫計時器**
</dt> <dd>

提供計時服務的元件，可與動畫管理員一起使用。 它會根據應用程式和系統負載或低電源模式，動態地節流畫面播放速率。 另請參閱：節流。

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**動畫變數** 
</dt> <dd>

可以動畫顯示的值。 動畫變數可用來代表可見物件的位置、大小、旋轉、透明度和其他品質。

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**取消**
</dt> <dd>

從排程中移除分鏡腳本，再開始播放的流程。

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**壓縮**
</dt> <dd>

分鏡腳本對時間的認知。 系統會藉由傳遞比系統時鐘更快的輸入時間值，來增加分鏡腳本進行的速率。

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**結論**
</dt> <dd>

指示分鏡腳本結束任何無限迴圈的進程。 如果迴圈已開始，則目前的反復專案將會完成，然後再播放分鏡腳本的其餘部分。 否則，將會完全略過腳本的已迴圈部分。

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**框架** 
</dt> <dd>

電影或動畫中的單一影像。

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**畫面播放速率** 
</dt> <dd>

每秒顯示的畫面格數。 畫面播放速率越高，圖片中的動作通常就越流暢。

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolator**
</dt> <dd>

程式設計物件，它會執行值的數學插補以及轉換變數的速度。

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**關鍵 幀**
</dt> <dd>

分鏡腳本內的時間點，可以相對於腳本的開頭、相對於另一個主要畫面格，或在轉換的結束時間指定，並且用來指定其他轉換的開始和結束時間，或分鏡腳本內的迴圈。

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**環**
</dt> <dd>

重複播放的兩個主要畫面格之間的分鏡板區段。 迴圈可能會無限次數或無限期地播放。

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**優先順序比較** 
</dt> <dd>

用戶端定義的程式碼，用來比較兩個分鏡腳本，一個已排程，另一個則是要排程的分鏡腳本，以判斷其相對優先權。 排程的分鏡腳本可能會被修剪、壓縮、取消或結束，以啟用較高優先順序的分鏡腳本排程。

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>分鏡腳本 
</dt> <dd>

每一組動畫轉換會彼此同步處理。

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**標記** 
</dt> <dd>

由整數識別碼和 COM 物件所組成的配對，可供應用程式用來識別特定動畫管理員範圍內的動畫變數和分鏡腳本。

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**節流** 
</dt> <dd>

動態調整動畫的畫面播放速率以符合特定需求。 節流有助於確保動畫是以一致的畫面播放速率轉譯，同時將系統資源的使用降至最低，而不是所需或有用的速率。

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**刻度** 
</dt> <dd>

通常會觸發單一畫面格呈現的計時器事件。

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**轉換** 
</dt> <dd>

定義動畫變數在一段時間內漸進式更新的結構。

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**修剪**
</dt> <dd>

使用較高優先順序的分鏡腳本，來優先使用動畫變數的動畫控制項。 如果在一或多個變數上修剪分鏡腳本會導致腳本提前結束，則會被視為截斷。 另請參閱：截斷。

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**截斷**
</dt> <dd>

藉由對一或多個較高優先順序的分鏡腳本進行動畫處理的一或多個變數的控制權，提前結束分鏡腳本。 另請參閱：修剪。

</dd> </dl>

 

 




