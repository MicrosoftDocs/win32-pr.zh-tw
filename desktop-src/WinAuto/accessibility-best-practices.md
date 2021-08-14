---
title: 協助工具最佳作法
description: 執行本節所述的最佳作法有助於確保使用輔助技術產品的人員可以存取您的應用程式。
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f596378c55b5f99af5b24fa60a23d980407392298fe2ad656579730fbab709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327868"
---
# <a name="accessibility-best-practices"></a>協助工具最佳作法

執行本節所述的最佳作法有助於確保使用輔助技術產品的人員可以存取您的應用程式。 其中許多最佳做法著重于良好的 UI 設計。 每個最佳作法都包含控制項或應用程式的執行資訊。 在許多情況下，這些最佳作法的大部分工作都已包含在控制項中。

本主題包含下列各節。

-   [以程式設計方式存取](#programmatic-access)
    -   [啟用以程式設計方式存取所有 UI 項目和文字](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [在 UI 物件、框架和頁面上放置名稱、標題和描述](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [確定所有 UI 活動都會觸發程式設計事件](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [使用者設定](#user-settings)
    -   [遵循所有系統範圍設定並不會干擾協助工具功能](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [視覺 UI 設計](#visual-ui-design)
    -   [不 Hard-Code 色彩](#do-not-hard-code-colors)
    -   [支援高對比和所有系統的顯示屬性](#support-high-contrast-and-all-system-display-attributes)
    -   [確定所有 UI 正確地依 DPI 設定值縮放比例](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [鍵盤流覽](#keyboard-navigation)
    -   [提供所有 UI 項目的鍵盤介面](#provide-keyboard-interface-for-all-ui-elements)
    -   [顯示鍵盤焦點](#show-the-keyboard-focus)
    -   [支援巡覽標準和強大的巡覽配置](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [不要讓滑鼠位置干擾鍵盤巡覽](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [多重模式介面](#multi-modal-interface)
    -   [對於非文字項目提供使用者可選取的對等項目](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [使用色彩，但是也提供色彩的替代方案](#use-color-but-also-provide-alternatives-to-color)
    -   [藉由與裝置無關的呼叫使用標準輸入的 API](#use-standard-input-apis-with-device-independent-calls)
-   [相關主題](#related-topics)

## <a name="programmatic-access"></a>程式設計存取

本節中的最佳作法 enure 輔助技術產品具有適當的程式設計方式來存取 UI 資訊和功能。

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>啟用以程式設計方式存取所有 UI 項目和文字

您應用程式的 UI 元素必須以程式設計方式存取輔助技術產品。 所有 UI 元素都必須有標籤，它們必須公開所有屬性值，而且必須引發所有適當的事件。 在標準 Windows 控制項中，大部分的工作都已經透過 Microsoft 消費者介面自動化和 Microsoft Active Accessibility proxy 物件完成。 但是，自訂控制項需要額外的工作，以確保它們完全公開，讓輔助技術廠商可以識別和操作您應用程式 UI 的元素。

遵循此最佳做法可讓輔助技術廠商識別和操作您產品 UI 的元素。

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>在 UI 物件、框架和頁面上放置名稱、標題和描述

由於輔助技術產品（尤其是螢幕讀取器）使用標題來瞭解框架、物件或頁面在導覽配置中的位置，標題必須有很高的描述性。 好用的描述性標題可讓輔助技術產品識別和操作控制項和應用程式中的 UI 元素。 例如，如果使用者已深入流覽到特定區域，則「Microsoft 網頁」的網頁標題就毫無用處。 描述性的標題對於失明和依賴螢幕讀取器的使用者來說很重要。

遵循此最佳做法可讓輔助技術產品識別和操作範例控制項和應用程式中的 UI。

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>確定所有 UI 活動都會觸發程式設計事件

每當 UI 元素的狀態或外觀發生變更時，您的應用程式應該會引發事件。

遵循此最佳做法可讓輔助技術產品接聽 UI 中的變更，並通知使用者這些變更。

## <a name="user-settings"></a>使用者設定

本節中的最佳做法可確保該控制項或應用程式不會覆寫使用者設定。

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>遵循所有系統範圍設定並不會干擾協助工具功能

使用者可以使用主控台設定一些全系統旗標;您可以透過程式設計方式來設定其他旗標。 不應該由控制項或應用程式變更這些設定。 此外，應用程式必須支援主機作業系統的協助工具設定。

遵循這個最佳做法可讓使用者設定協助工具設定，並了解這些設定不會由應用程式所變更。

## <a name="visual-ui-design"></a>視覺 UI 設計

本節中的最佳做法可確保控制項或應用程式有效地使用色彩和影像，並可供輔助技術產品使用。

### <a name="do-not-hard-code-colors"></a>不 Hard-Code 色彩

色盲、視力不佳或使用黑白螢幕的人可能無法使用色彩為硬式編碼的應用程式。

遵循這個最佳做法可讓使用者根據個人需求調整色彩組合。

### <a name="support-high-contrast-and-all-system-display-attributes"></a>支援高對比和所有系統的顯示屬性

應用程式不應中斷或停用使用者選取的系統範圍對比設定、色彩選擇或其他系統範圍的顯示設定和屬性。 使用者採用的系統範圍設定可增強應用程式的可及性，所以應用程式不應停用或忽略它們。 應該在正確的前景背景組合中使用色彩，以提供適當的對比。 不應混用不相關的色彩，而且不應反轉色彩。

許多使用者需要特定的高對比組合，例如在黑色背景上的白色文字。 如在白色背景上的黑色文字一樣反轉繪製，會造成背景滲出到前景，可能會使某些使用者閱讀困難。

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a>確定所有 UI 正確地依 DPI 設定值縮放比例

請確定所有的 UI 元素都可以依每英寸的任何點 (DPI) 設定來適當地調整。 此外，請確定 UI 元素能容納在 1024 x 768 的螢幕中，每英寸都有120點 (DPI) 。

## <a name="keyboard-navigation"></a>鍵盤導覽

本節中的最佳做法可確保依賴鍵盤的使用者可以存取所有的應用程式功能。

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>提供所有 UI 項目的鍵盤介面

Tab 鍵停止，特別是在仔細規劃時，讓使用者可以用另一種方式流覽 UI。

應用程式應該提供下列鍵盤介面：

-   使用者可以與之互動的所有控制項（例如按鈕、連結或清單方塊）的 Tab 鍵停止。
-   邏輯索引標籤順序。

### <a name="show-the-keyboard-focus"></a>顯示鍵盤焦點

使用者需要知道哪個物件具有鍵盤焦點，這樣他們才可以預期按鍵的效果。 若要醒目提示鍵盤焦點，請使用色彩、字型或圖形，例如矩形或縮放比例。 若要以可聽見的方式提示鍵盤焦點，請變更音量、音高或音調品質。

為了避免混淆，應用程式應隱藏所有視覺焦點指標，以及將位於非使用中視窗 (或窗格) 中的選取項目變暗。

應用程式應以鍵盤焦點執行下列動作：

-   一個專案應該一律具有鍵盤焦點。
-   鍵盤焦點應該是可見且顯而易見的。
-   選取專案及/或焦點專案應以視覺化方式反白顯示。

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>支援巡覽標準和強大的巡覽配置

鍵盤導覽的不同層面提供不同的方式讓使用者流覽 UI。

應用程式應該提供下列鍵盤介面：

-   快速鍵，以及所有命令、功能表和控制項的加底線存取金鑰。
-   重要連結的鍵盤快速鍵。
-   所有功能表項目都有存取金鑰;所有按鈕都有快速鍵，所有命令都有快速鍵。

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>不要讓滑鼠位置干擾鍵盤巡覽

滑鼠位置不應干擾鍵盤巡覽。 例如，如果滑鼠置於某個位置，而且使用者正在以鍵盤巡覽，則不應發生滑鼠點選，除非這是由使用者啟始的。

## <a name="multi-modal-interface"></a>多重模式介面

本節中的最佳做法可確保應用程式 UI 包含視覺元素的替代方案。

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>對於非文字項目提供使用者可選取的對等項目

對於每個非文字項目，提供文字、文字記錄或音訊描述之使用者可選取的對等項目，如替代文字、標題或視覺化回饋。

非文字元素涵蓋範圍廣泛的 UI 元素，包括：影像、影像地圖區域、動畫、applet、框架、腳本、圖形按鈕、音效、獨立音訊檔案和影片。 如果非文字元素包含使用者需要存取的視覺資訊、語音或一般音訊資訊，以瞭解 UI 的內容，就很重要。

### <a name="use-color-but-also-provide-alternatives-to-color"></a>使用色彩，但是也提供色彩的替代方案

請使用色彩來增強及強調，或再次提醒以其他方式顯示的資訊，但請勿單獨使用色彩傳達資訊。 色盲或使用單色顯示器的使用者需要色彩的替代方案。

### <a name="use-standard-input-apis-with-device-independent-calls"></a>藉由與裝置無關的呼叫使用標準輸入的 API

與裝置無關的呼叫可確保所有輸入裝置均視為相同，同時提供具有 UI 所需資訊的輔助技術產品。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows自動化 API 總覽](windows-automation-api-overview.md)
</dt> </dl>

 

 




