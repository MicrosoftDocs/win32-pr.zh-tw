---
title: " (Windows 協助工具功能的詞彙) "
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16679c63f0716058e53c7c9d164a24593c481dff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967510"
---
# <a name="glossary-windows-accessibility-features"></a> (Windows 協助工具功能的詞彙) 

## <a name="a"></a>A

<dl> <dt>

**存取金鑰**
</dt> <dd>

控制項標籤文字中的加底線字元。

</dd> <dt>

**協助工具輔助**
</dt> <dd>

也稱為輔助技術;專門用來處理電腦作業系統以因應特定障礙的程式，例如有限範圍的動作或失明。 產品包含較大的鍵盤、眼睛操作鍵盤、語音輸入公用程式、螢幕小鍵盤，以及可以將文字轉換成語音或動態盲文顯示器的產品。 如需詳細資訊，請參閱 [輔助技術產品](https://www.microsoft.com/enable/at/default.aspx)。

</dd> <dt>

**可存取的物件**
</dt> <dd>

任何會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的使用者介面專案，而且具有描述物件名稱、畫面位置，以及協助工具協助工具所需之其他資訊的屬性。 如需詳細資訊，請參閱 [可存取的物件](accessible-objects.md)。

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**子項目**
</dt> <dd>

請參閱 [*簡單元素*](uiauto-glossary.md)。

</dd> <dt>

**客戶**
</dt> <dd>

任何使用消費者介面自動化或 Microsoft Active Accessibility 來存取、識別或操作應用程式之使用者介面元素的程式;用戶端包括協助工具輔助、自動化測試控管，以及某些以電腦為基礎的定型應用程式。 如需詳細資訊，請參閱 [Active Accessibility 的運作方式](how-active-accessibility-works.md)。

</dd> <dt>

**用戶端提供者**
</dt> <dd>

由消費者介面自動化用戶端所執行的軟體元件，可取得不支援或不完全支援消費者介面自動化之應用程式的 UI 相關資訊。 一般而言，用戶端提供者 (proxy) 透過傳送和接收 Windows 訊息，在整個進程界限上與應用程式進行通訊。

</dd> <dt>

**container**
</dt> <dd>

也稱為父系;對應至一個或多個簡單元素的可存取物件;例如，清單方塊的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件是清單專案的父系。

</dd> <dt>

**控制項模式**
</dt> <dd>

在消費者介面自動化中，描述控制項的部分功能的設計執行。 這項功能可以包含控制項的視覺外觀，以及它可以執行的動作。

</dd> <dt>

**控制項模式物件**
</dt> <dd>

COM 物件的執行時間實例，這個實例會公開一或多個控制項模式介面。

</dd> <dt>

**控制項模式提供者**
</dt> <dd>

實作為一或多個控制項模式介面的軟體元件。

</dd> <dt>

**自訂控制項**
</dt> <dd>

由使用者或協力廠商軟體廠商所撰寫的控制項，或是由使用者或協力廠商軟體廠商修改的系統定義控制項。

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**範圍 (空白範圍) 的退化文字範圍**
</dt> <dd>

物件，代表空的 (零字元) 範圍的文字。 退化文字範圍具有連續的端點，並指定兩個字元之間的點。

</dd> <dt>

**不連續的文字範圍**
</dt> <dd>

物件，表示多個不是實體連續的文字範圍。

</dd> <dt>

**停駐容器**
</dt> <dd>

允許以水準和垂直方式排列子項目（相對於停駐容器的界限，以及容器內的其他元素）的控制項。

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**事件接聽程式**
</dt> <dd>

已註冊的用戶端應用程式，可在發生特定 UI 變更時，接收來自消費者介面自動化或 Microsoft Active Accessibility 的通知。

</dd> <dt>

**事件通知**
</dt> <dd>

從消費者介面自動化提供者至用戶端的呼叫，提供者會向用戶端通知可能會影響 UI 專案狀態或外觀的事件。

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**篩選 \[ 條件\]**
</dt> <dd>

定義要包含在消費者介面自動化樹狀結構視圖中的消費者介面自動化專案類型。 另請參閱：原始視圖、控制項視圖和內容視圖。

</dd> <dt>

**片段根目錄**
</dt> <dd>

消費者介面自動化樹狀目錄之子樹之根節點的消費者介面自動化專案。 片段根目錄沒有父代，但裝載于其他架構中，通常是 Win32 視窗控制碼 (**HWND**) 。

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**主機**
</dt> <dd>

包含其他 UI 專案的 UI 元素，例如視窗或控制項。 主機會代表裝載的元素執行消費者介面自動化服務。

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**IAccessible**
</dt> <dd>

COM 介面，其中包含 Microsoft Active Accessibility 的所有方法和屬性。

</dd> <dt>

**IAccessible proxy**
</dt> <dd>

一種 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援，提供標準 UI 元素的預設協助工具資訊：使用者控制項、使用者功能表，以及來自 COMCTL 和 comctl32.dll 的通用控制項。 如需詳細資訊，請參閱 [IAccessible](iaccessible-proxies.md)proxy。

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**邏輯導覽**
</dt> <dd>

兩個 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 瀏覽模式的其中一種，用戶端會探索 Microsoft Active Accessibility 的物件階層 (下一個、上一個、父系、第一個子系、最後一個子) 。

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**marshaling**
</dt> <dd>

封裝和傳送跨進程界限的介面參數。

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**原生執行**
</dt> <dd>

執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的使用者介面元素所提供的支援類型。

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**全螢幕模型**
</dt> <dd>

此模型是螢幕上物件的資料庫，其中包含其屬性和其空間關聯性。

</dd> <dt>

**OLEACC**
</dt> <dd>

動態連結程式庫，可提供 Microsoft Active Accessibility 執行時間，並管理來自 Microsoft Active Accessibility 用戶端的要求。

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

也稱為容器;對應至一個或多個簡單元素的可存取物件;例如，清單方塊的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件是清單專案的父系

</dd> <dt>

**預留位置自動化元素**
</dt> <dd>

消費者介面自動化元素，表示消費者介面自動化樹狀目錄中的虛擬化專案。 通常，預留位置尚未載入所有消費者介面自動化屬性的資料，而且只需要執行 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。

</dd> <dt>

**屬性變更事件**
</dt> <dd>

當屬性的值變更時觸發的事件。 用戶端會註冊以接收特定屬性變更的事件，並在這些事件發生時，消費者介面自動化通知已註冊的用戶端。

</dd> <dt>

**提供者介面**
</dt> <dd>

由消費者介面自動化提供者所執行之公用方法的集合。

</dd> <dt>

**代理**
</dt> <dd>

請參閱 [*IAccessible proxy*](uiauto-glossary.md)。

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**原始視圖**
</dt> <dd>

消費者介面自動化樹狀結構中，桌面為其根目錄的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 物件完整樹狀目錄。 原始視圖會緊密遵循應用程式的原生程式設計結構，因此是最精確的 UI 結構視圖。 它也是樹狀結構其他檢視的建置基底。

</dd> <dt>

**實現專案**
</dt> <dd>

已將完整資訊載入記憶體中的 UI 專案，可讓消費者介面自動化建立專案的 Automation 元素。

</dd> <dt>

**執行時間識別碼**
</dt> <dd>

整數陣列，識別消費者介面自動化專案的執行中實例。 識別碼在產生它的桌面 UI 中是唯一的。

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**safe 陣列**
</dt> <dd>

自我描述的資料類型，用於宣告用來建立 COM 元件的陣列。 除了資料，安全陣列也包含其維度的數目和界限的相關資訊。

</dd> <dt>

**範圍**
</dt> <dd>

從基底元素開始，定義視圖的範圍。

</dd> <dt>

**伺服器**
</dt> <dd>

任何使用 Microsoft Active Accessibility 來公開其使用者介面相關資訊的控制項、模組或應用程式

</dd> <dt>

**伺服器端提供者**
</dt> <dd>

一種軟體元件，會根據不支援原生消費者介面自動化的 UI 架構，公開 UI 專案的相關資訊。 伺服器端提供者 (原生提供者) 透過將 COM 介面公開給消費者介面自動化核心系統（其會服務來自用戶端的要求），在整個進程界限之間與用戶端應用程式進行通訊。

</dd> <dt>

**simple 元素**
</dt> <dd>

也稱為子項目;任何與其他元素共用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件並依賴該 **IAccessible** 物件來公開其屬性的使用者介面元素。 如需詳細資訊，請參閱 [簡單元素](simple-elements.md)。

</dd> <dt>

**空間導覽**
</dt> <dd>

兩個 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 瀏覽模式的其中一種，用戶端會根據畫面上的位置，從某個使用者介面專案移至另一個使用者介面專案， (向上、向下、向左、右) 。

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Text Services Framework (TSF)**
</dt> <dd>

可調整的系統架構，可在桌上型電腦和應用程式中啟用自然語言服務和 advanced text 輸入。

</dd> <dt>

**文字單位**
</dt> <dd>

預先定義的文字單元 (字元、單字、線條或段落) 用於流覽文字範圍的邏輯區段。

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**消費者介面自動化用戶端**
</dt> <dd>

使用消費者介面自動化的輔助技術應用程式，可讓您以程式設計方式存取應用程式使用者介面中的 UI 元素。 用戶端會向終端使用者顯示 UI 元素的相關資訊。 自動化測試腳本也會被視為消費者介面自動化用戶端。

</dd> <dt>

**消費者介面自動化核心**
</dt> <dd>

執行消費者介面自動化架構的執行時間元件。

</dd> <dt>

**消費者介面自動化元素**
</dt> <dd>

由 COM 物件表示的 UI 專案，該物件會執行消費者介面自動化提供者介面，並將 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面公開給消費者介面自動化的用戶端。

</dd> <dt>

**消費者介面自動化架構**
</dt> <dd>

整數的 Windows 元件，可支援以程式設計方式存取桌面上大部分的 UI 元素。 它可讓您的輔助技術產品（例如螢幕讀取器）提供使用者介面的相關資訊給使用者，以及透過標準輸入以外的方式操作 UI。 消費者介面自動化也可讓自動化測試腳本與 UI 互動。

</dd> <dt>

**消費者介面自動化節點**
</dt> <dd>

已取代。 請參閱消費者介面自動化元素。

</dd> <dt>

**消費者介面自動化提供者**
</dt> <dd>

消費者介面自動化介面的執行，可公開 UI 專案的程式設計資訊。 此提供者會將這項資訊提供給消費者介面自動化架構，以回應消費者介面自動化用戶端要求。

</dd> <dt>

**消費者介面自動化樹狀結構**
</dt> <dd>

Windows 桌面上所有消費者介面自動化元素的階層式標記法。 樹狀結構包含代表目前桌面的根項目，以及其子項目代表應用程式視窗的根項目。 每個子專案都可以包含代表 UI 片段的元素，例如功能表、按鈕、工具列和清單方塊。 這些元素可以包含專案，例如清單專案。

</dd> <dt>

**UI 架構**
</dt> <dd>

管理子控制項、點擊測試，以及在螢幕區域中轉譯的元件。

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**視圖識別碼**
</dt> <dd>

值，這個值會識別可供執行控制項模式之消費者介面自動化專案使用的視圖。 這種類型的元素會提供，而且可以在相同資訊集或子控制項的多個標記法之間切換。

</dd> <dt>

**虛擬化專案**
</dt> <dd>

只有在需要時才會載入至記憶體的 UI 元素，通常是在螢幕上顯示專案時。 虛擬專案是由消費者介面自動化樹狀結構中的預留位置自動化元素表示。

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**WinEvents) 的視窗事件 (**
</dt> <dd>

用來通知用戶端可存取物件以某種方式變更的事件種類。

</dd> <dt>

**以視窗為基礎的元素**
</dt> <dd>

消費者介面自動化專案，表示有自己的 Win32 視窗控制碼 (**HWND**) 的 UI 專案。

</dd> </dl>

 

 




