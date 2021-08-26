---
description: Windows安裝套裝程式含的功能，可讓安裝套件開發人員撰寫圖形化使用者介面， (GUI) 在安裝期間對使用者顯示。
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: 關於消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff4613e82bc25a0a9555904a6bab276b31e16642186401bbb5cc0caff58e973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996978"
---
# <a name="about-the-user-interface"></a>關於消費者介面

Windows安裝套裝程式含的功能，可讓安裝套件開發人員撰寫圖形化使用者介面， (GUI) 在安裝期間對使用者顯示。 此使用者介面可以展示 [使用者介面 wizard 的行為](user-interface-wizard-behavior.md)、顯示對話方塊和公告欄，以及在安裝期間對使用者呈現互動式控制項。

安裝程式內部 UI 是透過 Windows Installer 本身內的一組資料庫資料表來管理和控制。 安裝程式只會提供一組用於處理錯誤和資訊訊息的預設對話方塊。 所有自訂對話方塊都必須由封裝作者建立。

沒有特定的 Windows Installer API 可讓套件作者以程式設計方式建立 UI。 您可以使用 Microsoft Windows API 以程式設計方式建立 UI;不過，建議套件作者使用提供的內部 UI。

安裝程式套件作者建立自訂對話方塊的方式，是將其自訂對話方塊的名稱輸入 \_ 對話方塊資料表的 "dialog" 資料行，並使用其餘的資料行來指定大小、位置和其他屬性。

Windows安裝程式也會執行封裝作者可放置在對話方塊上的一些標準控制項。 並非所有標準的 Microsoft Windows 控制項都可使用，而且無法建立自訂控制項以搭配安裝程式 UI 使用。

您可以在特定的對話方塊上建立控制項，方法是輸入對話方塊名稱、對話方塊資料表中對話方塊專案的主鍵、控制項資料表的第二個欄位，以及使用其餘的資料行來指定控制項的大小、位置和其他屬性。

現用控制項必須連結至 [ControlEvent 資料表](controlevent-table.md) 中的 ControlEvent，以允許使用者與安裝互動。 接收和顯示資訊的被動控制項必須訂閱 [EventMapping 資料表](eventmapping-table.md)中適當的 ControlEvent。

如需有關事件的詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。 請注意，如果在 ControlEvent 資料表中列出某個控制項，並且訂閱了 EventMapping 資料表中所列的事件，控制項就會發行 ControlEvent。

安裝期間的安裝程式 UI 會透過 UI 順序資料表來管理： [InstallUISequence 資料表](installuisequence-table.md)和 [AdminUISequence 資料表](adminuisequence-table.md)。 系統會根據起始安裝的最上層動作，執行下列其中一個順序資料表： [安裝](install-action.md)、系統 [管理員](admin-action.md)或 [公告](advertise-action.md)。

如需在 Windows Installer 中執行 UI 的詳細資訊，請參閱[使用消費者介面](using-the-user-interface.md)、[消費者介面架構](user-interface-schema.md)，以及對話方塊和控制項的個別主題。

 

 



