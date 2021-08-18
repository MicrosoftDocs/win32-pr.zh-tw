---
description: 本節主要在說明安裝套件開發人員如何使用安裝程式的資料庫和內部 UI)  (UI 來撰寫安裝使用者介面。
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: 使用使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2303ddcdf589b69abb819ab1cdee9060f4918c1bd238e161677da7987300bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995988"
---
# <a name="using-the-user-interface"></a>使用使用者介面

本節主要在說明安裝套件開發人員如何使用安裝程式的資料庫和內部 UI)  (UI 來撰寫安裝使用者介面。 如需內部和外部 UI 之間差異的詳細資訊，請參閱 [關於消費者介面](about-the-user-interface.md)。

若要在安裝期間顯示對話方塊序列或佈告欄，必須在適當的動作順序資料表的 [動作] 資料行中輸入對話方塊的名稱。 對話方塊的名稱必須出現在 [InstallUISequence](installuisequence-table.md) 或 [AdminUISequence 資料表](adminuisequence-table.md) 中，取決於 UI 是否已排程在 [ [安裝](install-action.md)]、[ [公告](advertise-action.md)] 或 [系統 [管理員] 動作](admin-action.md)下執行。

雖然安裝程式支援撰寫自訂對話方塊和公告欄，但某些對話方塊序列也有一些保留名稱。 因為安裝程式會在執行某些動作時使用這些名稱，所以這些名稱只能搭配其保留的對話方塊類型使用。 這些保留名稱的清單，以及每個特殊對話方塊序列的描述都是在 [對話方塊](dialog-boxes.md)中提供。

您必須分別在 [對話](dialog-table.md) 和 [佈告欄](billboard-table.md) 資料表中指定 UI 中每個對話方塊或佈告欄的屬性。 您也必須藉由設定 [對話方塊的樣式位](dialog-style-bits.md) 旗標，在對話方塊資料表中指定每個對話方塊的樣式。

控制項和文字必須加入至對話方塊，而且必須系結至 [控制項，才能](controlevent-overview.md)讓使用者與安裝程式互動。 如需如何將控制項加入對話方塊的詳細資訊，請參閱 [加入控制項和文字](adding-controls-and-text.md) 。

Windows安裝程式內部 UI 處理常式可以選擇性地顯示或隱藏對話方塊，以控制安裝期間使用者互動的層級。 這些使用者互動層級稱為「完整」、「精簡」、「基本」和「無」。 請參閱 [消費者介面層級](user-interface-levels.md)。 如需這些 UIlevels 的完整說明。

有兩種方法可以設定 UI 層級。 UI 層級可透過呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)，以程式設計方式設定，而 **MsiSetInternalUI** 的第一個參數會指定 ui 層級。 套件開發人員也可以使用 [命令列選項](command-line-options.md) "/q" 來設定 UI 層級。

每個 UI 層級的行為取決於封裝開發人員撰寫 .msi 檔。 內部 UI 的作者對於這些層級對封裝的行為有彈性。 這些層級的可用性取決於撰寫安裝套件。 作者必須在對話方塊和控制項資料表的使用者介面中，指定每個對話方塊和控制項。

-   完整的 UI 通常會展示 [使用者介面 wizard 的行為](user-interface-wizard-behavior.md)，例如包含 **下一個>>** 按鈕的序列中的每個對話方塊。 這種形式的 UI 對許多使用者來說很熟悉，而且是最常用來建立作者的 UI 類型。 安裝程式會顯示對話方塊的邏輯順序，並提示使用者與位於每個對話方塊的控制項互動。
-   縮減的 UI 通常會抑制 wizard 行為的顯示。
-   基本 UI 通常只會顯示使用者的進度訊息。
-   [無] 的 UI 層級表示無訊息安裝。

Windows安裝程式會在[ProgressBar 控制項](progressbar-control.md)中提供唯一的進度列指示器，讓使用者在安裝完成之前，對使用者顯示總剩餘時間的估計值。 如需進度列的詳細資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)。

UI 作者應該為所有使用者提供其應用程式或產品的協助工具。 若要深入瞭解 Active Accessibility 和 Windows Installer，請參閱[協助工具](accessibility.md)。

如需撰寫使用者介面的詳細資訊，請參閱 [新增控制項和文字](adding-controls-and-text.md)、 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)、撰寫 [磁片提示訊息](authoring-disk-prompt-messages.md)、 [撰寫條件式「請稍候 ...」訊息方塊](authoring-a-conditional-please-wait-------message-box.md)，並 [預覽消費者介面](previewing-the-user-interface.md)。 如需作者公告欄的詳細資訊，請參閱 [在非強制回應對話方塊上顯示公告欄](displaying-billboards-on-a-modeless-dialog.md)

從 Windows Installer 4.5 開始，自訂使用者介面可以內嵌在 Windows Installer 封裝內。 如需內嵌自訂 UI 的範例，請參閱 [使用內嵌 ui](using-an-embedded-ui.md)。

 

 



