---
title: Windows 動畫總覽
description: 本總覽提供 Windows 動畫管理員的簡介，並著重于重要元件和概念。
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows 動畫視窗動畫、總覽
- 動畫管理員物件視窗動畫，說明
- 動畫變數 Windows 動畫，說明
- 動畫計時器物件視窗動畫，說明
- 計時系統視窗動畫
- 上下文相關持續時間 Windows 動畫
- 符合 Windows 動畫的速度
- 爭用管理視窗動畫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a60b02b29d8d434cc93420f36c3cdca4428f94c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023575"
---
# <a name="windows-animation-overview"></a>Windows 動畫總覽

本總覽提供 Windows 動畫管理員的簡介，並著重于重要元件和概念。 如需分鏡腳本和轉換的詳細資訊，請參閱分鏡腳本 [總覽](storyboard-construction.md)。

本主題包含下列幾節：

-   [基本概念](#basic-concepts)
-   [Windows 動畫的元件](#components-of-windows-animation)
-   [Windows 動畫 API](#the-windows-animation-api)
-   [組態](#configurations)
    -   [應用程式驅動的動畫](#application-driven-animation)
    -   [計時器驅動動畫](#timer-driven-animation)
-   [Advanced 功能](#advanced-features)
    -   [爭用管理](#contention-management)
-   [相關主題](#related-topics)

## <a name="basic-concepts"></a>基本概念

*動畫* 是連續的靜止影像順序，會在播放時產生移動的假像。 在其使用者介面中使用互動式動畫可提供應用程式獨特的特性，以及改善使用者體驗。 動畫可協助您在使用者介面中傳達主要狀態變更，並協助管理使用者介面的複雜度。 動畫也可以新增到使用者對應用程式品質的認知。

例如，工作列中使用 Windows 動畫來協助您管理和存取檔案和程式，以及放大鏡來放大螢幕的不同部分，讓使用者更容易看見。

動畫的基礎單位是要進行動畫的視覺元素特性，以及該特性如何隨著時間而變更的描述。 應用程式可以建立各種特性的動畫，例如位置、色彩、大小、旋轉、對比和不透明度。

在 Windows 動畫中， *動畫變數* 表示要進行動畫的特性。 *轉換* 會描述動畫變數的值如何隨著動畫而變更。 例如，視覺元素可能會有指定其不透明度的動畫變數，而使用者動作可能會產生將該不透明度從50值轉換為100的轉換，表示從半透明到完全不透明的動畫。

分鏡 *腳本是一組在一* 段時間內套用至一或多個動畫變數的轉換。 應用程式會藉由建立和播放腳本，然後繪製離散框架的順序來顯示動畫，因為動畫變數的值會隨著時間而變更。

## <a name="components-of-windows-animation"></a>Windows 動畫的元件

Windows 動畫包含下列元件：

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>動畫管理員
</dt> <dd>

應用程式會使用動畫管理員物件來建立動畫變數和分鏡腳本、排程和控制動畫，以及在應用程式繪製每個畫面格之前更新狀態資訊。 單一動畫管理員物件通常會管理整個應用程式的所有動畫，因此可對所有已排程的分鏡腳本進行全域控制。

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>動畫變數
</dt> <dd>

在開始任何動畫之前，應用程式必須建立動畫變數物件。 動畫變數表示要進行動畫的視覺元素的其中一個層面。 變數是純量浮點值，雖然值可以四捨五入為整數值。

動畫變數的存留期通常與用來建立動畫的視覺元素相同。 建立變數時，會指定動畫變數的初始值。 之後，無法直接變更其值;您必須透過動畫管理員來更新它。

動畫變數可以透過 *標記* 來識別，也就是將整數識別碼與 COM 物件的指標配對。 標記不需要是唯一的，除非應用程式使用它來搜尋變數。 根據預設，動畫變數沒有標記，而任何讀取其標記的嘗試都將會失敗，直到已設定一個標記為止。

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>計時系統
</dt> <dd>

Windows 動畫包含時間系統，可協助確保動畫是以平滑且一致的畫面播放速率轉譯，同時也可減少系統資源忙碌時的系統資源使用方式。 *計時器* 會自動指出一小段時間（稱為 *滴答*），以協助管理動畫呈現。 計時系統會監視整體系統轉譯 *效能，並* 以動態方式增加或減少刻度的頻率來調整動畫。 應用程式可讓計時器驅動動畫管理員，並且可以註冊處理常式，以便在管理員更新每個刻度之前和之後收到通知。 應用程式可以為計時器指定可接受的最小動畫畫面播放速率，並且在動畫的實際畫面播放速率低於此速率時收到通知。

若要節省系統資源，您可以設定計時器，在沒有任何動畫發生時將其停用。

</dd> </dl>

## <a name="the-windows-animation-api"></a>Windows 動畫 API

Windows 動畫 API 是單一執行緒的 COM 型 API，可為開發人員提供下列功能：

-   動畫管理員物件 [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))，用於建立動畫物件和控制動畫
-   動畫變數和分鏡腳本
-   立即可用的轉換基礎程式庫 [**UIAnimationTransitionLibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85))
-   計時器物件（ [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))），用來判斷目前的時間，以及選擇性地驅動動畫
-   用於監視動畫狀態和進度的事件攔截

如需完整的 API 參考，請參閱 [Windows 動畫參考](windows-animation-reference.md)。 如需範例程式碼，請參閱 [Windows 動畫](using-windows-animation.md) 工作和 [windows 動畫範例](windows-animation-samples.md)。

## <a name="configurations"></a>設定

應用程式必須在排程新動畫之前取得目前的時間。 以下是 Windows 動畫所支援的計時機制：

-   [應用程式驅動的動畫](#application-driven-animation)
-   [計時器驅動動畫](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven 動畫

使用硬體加速圖形 API 的應用程式可以與監視器重新整理頻率進行同步處理，以轉譯平滑動畫。 或者，應用程式可以使用自己的計時機制，來判斷何時繪製動畫的每個畫面格。 在任一種情況下，應用程式都會告知動畫管理員何時更新其狀態。 動畫計時器仍然可以用來判斷具有高精確度的目前時間，以動畫管理員所需的單位為單位。

下圖顯示當應用程式直接驅動動畫更新時，應用程式與 Windows 動畫元件之間的互動。

![此圖顯示應用程式直接驅動動畫更新時，應用程式與 windows 動畫元件之間的互動。](images/animationupdates.png)

在最簡單的設定中，應用程式會在每次螢幕重新整理時重繪所有專案，即使沒有播放動畫也是一樣。 為了避免浪費的工作，應用程式可以註冊管理員事件處理常式，以便在有動畫排程時收到通知，並且可以偵測排程是空的，讓它可以停止重繪。

### <a name="timer-driven-animation"></a>Timer-Driven 動畫

應用程式可能會讓動畫計時器告知動畫管理員何時更新其狀態，而且只會在發生每項更新時收到通知，而不是直接更新動畫管理員。 這種方法建議用於舊版圖形 Api。 一般而言，如果可以與監視器重新整理頻率進行同步處理，最好是這麼做，並使用應用程式驅動的動畫。

下圖顯示當動畫計時器驅動動畫更新時，應用程式與 Windows 動畫元件之間的互動。

![此圖顯示當動畫計時器驅動動畫更新時，應用程式與 windows 動畫元件之間的互動。](images/animationtimerupdates.png)

計時器可以設定為只有在已排程動畫時才執行;這麼做只是在計時器和動畫管理員連接時傳遞特定參數的簡單做法。

## <a name="advanced-features"></a>進階功能

除了支援動畫的基本基礎之外，Windows 動畫還支援數種先進的動畫技術，包括：

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*區分內容的持續時間*
</dt> <dd>

轉換的持續時間不需要固定;您可以根據轉換開始時的動畫變數值和速度來決定此值。

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*速度相符*
</dt> <dd>

如果移動物件的位置和速度在值之間沒有立即跳躍，移動物件的位置和速度通常會更適合眼睛。 當新的分鏡腳本中斷目前現正播放的腳本時，速度比對可讓新的分鏡腳本在上一次結束的位置順利挑選。

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*爭用管理*
</dt> <dd>

如果兩個分鏡腳本需要同時更新相同的動畫變數，則會發生排程衝突。 Windows 動畫可讓應用程式判斷任何兩個分鏡腳本的相對優先權，而不需要每個分鏡腳本有特定的數值優先順序。

</dd> </dl>

### <a name="contention-management"></a>爭用管理

開發人員可以執行 *優先順序比較* 回呼，以比較已排程之分鏡腳本的優先順序以及已在排程中的分鏡腳本。 執行優先順序比較的應用程式可以使用任何慣用的邏輯來判斷分鏡腳本預先 empts 另一個的時間。 為了解決排程衝突，Windows 動畫會以下列順序要求應用程式執行下列動作：

-   **取消已排程的分鏡腳本。** 如果排定的分鏡腳本尚未開始播放，它可能會取消並立即從排程中移除。
-   **修剪排程的分鏡腳本。** 當新的分鏡腳本修剪排程的分鏡腳本時，排程的分鏡腳本會在新的腳本開始建立動畫時立即停止影響變數。 系統會比對速度，讓新的分鏡腳本能夠順暢地挑選前一個。
-   **結束排程的分鏡腳本。** 只有當分鏡腳本包含了無限期重複的迴圈時，才會結束。 如果腳本在結束時為這類迴圈，則目前的重複項會完成，而腳本的其餘部分則會播放。 如果在分鏡腳本結束時，迴圈尚未開始，則會完全略過迴圈。
-   **壓縮已排程的分鏡腳本。** 如果無法選擇修剪或取消已排程的分鏡腳本，則可以完成腳本。 Windows 動畫引進了可將排程的分鏡腳本 (的時間以及在) 之前排定的任何分鏡腳本，讓變數更快達到其最終狀態的可能性。 套用壓縮時，會暫時加速受影響的分鏡腳本，讓它們的播放速度更快。

如果註冊的優先順序比較物件不允許上述任何動作，則嘗試排程新的分鏡腳本會失敗。 根據預設，所有的分鏡腳本都可以修剪、結束或壓縮以防止失敗，但無法取消任何。

下圖顯示分鏡腳本的生命週期，使用 UI 動畫分鏡腳本 [**\_ \_ \_ 狀態**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) 列舉所定義的狀態。 應用程式會使用 Windows 動畫 API 來建立分鏡腳本，並提交以進行排程。 動畫管理員會排定分鏡腳本並管理動畫。

![顯示動畫管理員如何排程腳本和管理動畫的圖表。](images/statediagram.png)

如需分鏡腳本排程和管理的詳細資訊，請參閱分鏡腳本 [總覽](storyboard-construction.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 動畫參考](windows-animation-reference.md)
</dt> <dt>

[Windows 動畫範例](windows-animation-samples.md)
</dt> <dt>

[Windows 動畫工作](using-windows-animation.md)
</dt> </dl>

 

 