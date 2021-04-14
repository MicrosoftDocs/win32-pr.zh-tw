---
description: 本主題提供多語系消費者介面 (MUI) 技術的概念，以及它為啟用多語系使用者體驗所提供的平臺支援，以及它為 Windows 生態系統提供的優點。
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: MUI 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553139"
---
# <a name="overview-of-mui"></a>MUI 總覽

本主題提供多語系消費者介面 (MUI) 技術的概念，以及它為啟用多語系使用者體驗所提供的平臺支援，以及它為 Windows 生態系統提供的優點。

在此頁面上：

-   [多語系計算的需求](#the-need-for-multilingual-computing)
-   [MUI 在啟用多語系運算的角色](#the-role-of-mui-in-enabling-multilingual-computing)
-   [MUI 的核心概念](#core-concepts-of-mui)
-   [Windows 中的 MUI 記錄](#history-of-mui-in-windows)
-   [MUI 技術的優點](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>多語系計算的需求

為了受益于國際市場所呈現的成長機會，Microsoft 的平臺和應用程式支援比以往更多的語言、文化特性和市場。

除了增加全球化趨勢，語言、文化特性和市場細節仍與國際使用者非常相關。 下圖顯示非英文的喇叭仍占世界人口的91.5%。

![包含三個區段的圓形圖;標示為「非英文喇叭91.5%」的那個會大幅大於另二個組合](images/overview-of-mui-fig1.gif)

全球有193個國家/地區，以及過去使用的6900種已知生活語言。 無論其角色是世界的商務語言，英文都只會以第一或第二種語言的世界人口8.5% 來說。 為了將原生資訊提供給全球人口的94%，這項資訊必須在 347 (大約有5% 的全球語言，且至少有一百萬個喇叭的 ) 。 這種情況更是如此，因為全球化趨勢已提高這些使用者對其市場的技術及其可用性的期望。

以更多語言當地語系化軟體的需要多年來，Microsoft 現在提供比以往更多語言的 Windows Vista 和其他產品。 這種演進功能對 Microsoft Windows 特別明顯，因為它已從使用 windows 98 支援30種語言到幾乎100版的 Windows Vista，如下列橫條圖所示。

![橫條圖顯示 windows vista 中比 windows 98 或 windows xp 更大的語言數目](images/overview-of-mui-fig2.gif)

*圖 2-Microsoft Windows 版本支援的語言數目*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>MUI 在啟用多語系運算的角色

如上一節所述， [全球化](glossary-for-understanding-mui.md) 和 [當地語系化](glossary-for-understanding-mui.md) 應用程式已成為更全球整合世界的必要項。 尤其是，當越來越多的企業在內部或透過其商業網路進行全球化時，多語言應用程式的需求會大幅增加。 這是這些公司目前在全球部署這些應用程式時所面臨的障礙。

為 windows 作業系統提供更多語言支援，以及為 Windows 平臺建立的軟體應用程式，都需要新的策略，讓所有主要案例都能以最基本的工程額外負荷來實行。

MUI 技術的目標物件是開發人員和 Isv，以建立並支援 Windows 平臺的多語系應用程式。 MUI 對 Oem 和企業來說也很重要，因為他們可以利用它來部署 Windows 作業系統，並透過單一映射部署將應用程式新增至不同語言的電腦。

## <a name="core-concepts-of-mui"></a>MUI 的核心概念

MUI 背後的基本概念是將可 [當地語系化資源的儲存區與應用程式原始程式碼分開](mui-fundamental-concepts-explained.md)，如此一來，就能將任何多語系應用程式設計成與語言中立的核心二進位檔和一組語言特定當地語系化資源檔的組合。

當應用程式原始程式碼與當地語系化的資源分開儲存之後，您就可以輕鬆地根據系統、使用者和應用層級的使用者介面語言設定，動態地針對指定的應用程式內容 [載入適當的當地語系化資源](mui-fundamental-concepts-explained.md) 。

這些 MUI 的基本屬性有助於加速商務案例，例如：

-   透過實體區隔應用程式原始程式碼和可當地語系化的資源，改善使用者介面和說明內容的當地語系化模型。
-   將可當地語系化的資源視為動態內容，並根據 UI 語言設定和回溯喜好設定來載入它們。 這可實現下列案例：
    -   在執行時間從一個 UI 語言切換至另一個。
    -   建立涵蓋一組適用于 Oem 和企業之語言的區域或全球單一部署映射。

## <a name="history-of-mui-in-windows"></a>Windows 中的 MUI 記錄

針對 windows 作業系統層級的多語系使用者經驗，以及在 Windows 平臺上進行多語系應用程式開發的支援層級，在一段時間內和不同版本的 Windows 中都有演進。

[Windows Vista 之前](evolution-of-mui-support-across-windows-versions.md)的支援功能相當基本，具有單一語言的 windows 映射，以及在特定案例中附加元件多語系消費者介面套件的選項。 無語言應用程式的開發人員支援。

在[Windows vista](evolution-of-mui-support-across-windows-versions.md)中，MICROSOFT 對 mui 進行了大幅的投資，而 Windows vista 則是在 mui 平臺上從頭建立。 雖然這代表 Windows 當地語系化策略的主要進展，因為這是 Microsoft 在 windows 使用者、開發人員和客戶上提供更多語言的重要提供者，因此是最重要的一大步。 它提供數個主要優點，例如：

-   語言中立的作業系統，內建的 MUI 支援。
-   可設定的封裝、部署和安裝以支援多語系案例。
-   具有多種語言的單一映射部署。
-   改進的服務模型，可執行程式碼獨立于資源之外更新。
-   建立多語系應用程式的開發人員支援。

下表提供 MUI 的 Windows 平臺支援的詳細總覽：

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>類別</th>
<th>支援</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>支援的 Windows 版本 (OS 僅支援) </td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Windows 2000 伺服器系列</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Windows Server 2003 系列</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>支援的 Windows 版本 (OS & 應用程式支援) </td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>不支援的 Windows 版本</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows Me</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>MUI 技術的優點

MUI 會積極影響 Windows 生態系統的多個層面：

-   [開發人員的優點](benefits-of-mui-explained.md)：有許多優點會透過 MUI API 支援的可用性提供給應用程式開發人員，以建立以與核心 Windows 作業系統本身的多語系支援相同準則為模型的多語系應用程式。 這些優點包括：
    -   提供與作業系統本身提供一致之顯示語言體驗的能力。
    -   輕鬆擴充應用程式語言支援的能力。
    -   輕鬆維護及服務應用程式的能力。
    -   由 Oem 啟用應用程式的單一映射部署的能力。
-   [企業的優點](benefits-of-mui-explained.md)： MUI 為企業提供的主要優點是能夠透過單一安裝，在全球推出、支援及維護相同的多語系映射。 另一個重要的勝利是能夠支援多語系桌面，以提供與不同語言喜好設定的流暢互動。
-   [Oem 的優點](benefits-of-mui-explained.md)： oem 的主要優點是 MUI 啟用的單一映射安裝，支援多種語言，可讓您更有效地管理清查。 Oem 也受益于應用程式開發的 MUI 支援，因為它可讓它們在映射上提供加值應用程式，同時從單一映射安裝獲益，只要這些應用程式已啟用 MUI 即可。

 

 




