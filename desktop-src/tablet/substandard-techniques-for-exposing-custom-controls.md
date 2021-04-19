---
description: 公開自訂控制項的 substandard 技術描述。
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: 公開自訂控制項的 Substandard 技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988903"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>公開自訂控制項的 Substandard 技術

如果應用程式不支援 Microsoft Active Accessibility，則可能無法完全存取。 下列技巧轉譯控制項的部分相容：

-   使用 WM GETTEXT 訊息來查詢控制項時，傳回描述性字串 \_ 。 例如，允許對等按鈕控制項標示為 "Print" 的自訂對等專案傳回「列印按鈕」字串。 這會識別控制項類型和標籤。 相同的字串適用于標籤不是文字（例如印表機的圖形）的按鈕。 同樣地，您可以讓行為類似核取方塊的自訂控制項傳回標題字串「已啟用列印」核取方塊。
-   支援 WM \_ GETDLGCODE 訊息，識別支援的鍵盤輸入。 例如，允許編輯控制項的自訂對等，藉由傳回 \_ DLGC HASSETSEL 來處理 WM GETDLGCODE，方法是在 \_ 處理訊息來設定選取專案時，DLGC \_ WANTARROWS （如果它使用方向鍵），而 DLGC \_ WANTCHARS 表示它使用字元輸入。
    > [!Note]  
    > 只有具有自己的視窗控制碼的控制項可以回應 WM \_ GETTEXT 和 wm \_ GETDLGCODE 訊息。

     

為了避免協助工具協助工具的相容性問題，您應該在設計自訂控制項時，仔細遵循 Active Accessibility 的指導方針。 如需有關如何避免相容性問題與協助工具輔助的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md) 一節。

 

 
