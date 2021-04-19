---
description: 跨 Windows 版本的 MUI 支援演進
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: 跨 Windows 版本的 MUI 支援演進
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983738"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>跨 Windows 版本的 MUI 支援演進

-   [Windows Vista 之前](#before-windows-vista)
-   [Windows Vista 和其他](#windows-vista-and-beyond)
    -   [非語言相關/MUI 作業系統](#a-language-neutralmui-operating-system)
    -   [部署案例完全以 MUI 為基礎](#deployment-scenarios-are-fully-mui-based)
    -   [單一映射部署](#single-image-deployment)
    -   [改進的服務模型](#improved-servicing-model)
    -   [MUI 基礎結構](#mui-infrastructure)
    -   [語言管理](#language-management)
    -   [資源處理](#resource-handling)

## <a name="before-windows-vista"></a>Windows Vista 之前

在 Windows Vista 發行之前，Windows 隨附單一語言的映射，這表示每個當地語系化版本的 Windows 都包含單一語言的使用者介面。 MUI 是英文版作業系統的附加元件，且多語系消費者介面套件只能新增至某些英文版的 Windows。 當安裝在英文版的 Windows 上時，MUI 允許根據個別使用者的喜好設定，將作業系統的使用者介面語言變更為其中一種支援的語言。

MUI 套件模型不會公開應用程式的 MUI 支援。 雖然開發人員可以建立多語言的應用程式，但他們必須建立自己的機制來進行。

## <a name="windows-vista-and-beyond"></a>Windows Vista 和其他

在 Windows Vista 中，Microsoft 對 MUI 進行了大幅的投資。 Windows Vista 是在 MUI 平臺上從頭建立。 雖然這代表 Windows 當地語系化策略的一大進展，因為這是 Microsoft 為了提供比以往更多語言的 Windows，這對 Windows 使用者和客戶而言是一項很好的進步。

### <a name="a-language-neutralmui-operating-system"></a>非語言相關/MUI 作業系統

大部分的 Windows Vista 二進位檔都符合 MUI 規範，且可當地語系化的資料會與程式碼分開儲存。 這可提供彈性，因為您可以隨時新增不同的語言資料。

### <a name="deployment-scenarios-are-fully-mui-based"></a>部署案例完全以 MUI 為基礎

Windows Vista 封裝和安裝設計是以 MUI 為基礎，所有可當地語系化的資料都封裝在特定語言的套件中，而且每個語言套件都可以在不同的案例中部署。 例如，雖然適用于 Windows Vista 的零售版 Dvd 包含單一語言版本，但最終版本的使用者可以下載其他的 MUI 語言套件，並可從 [ **地區及語言選項** ] 控制台切換 UI 語言。 Enterprise edition 授權會取得所有語言，而且可以部署任何語言。

### <a name="single-image-deployment"></a>單一映射部署

企業客戶和 Oem 現在可以減少需要維護的映射數目，以便透過單一映射部署將 Windows 和應用程式部署到不同地區設定的電腦上。

在 Windows Vista 上使用 MUI，可將一個包含多種語言的映射部署到任何語言使用者，且使用者可以在設定期間，或在電腦的初始「全新體驗」中，判斷其慣用語言)  (。 尤其是，Oem 可以在新電腦上放置許多 UI 語言，讓使用者從歡迎中心中選取一個。 因此，在具有多個語言套件的映射中，安裝程式會顯示可用語言的清單，並讓使用者挑選其中一種語言。 然後，所有國際設定會設定為符合選取的語言或地區設定。

### <a name="improved-servicing-model"></a>改進的服務模型

相同的 QFE 或安全性修正套件現在可以安裝在任何語言系統之上。 這一點很重要，因為它可以更快速地解決安全性問題，並讓所有的國際使用者都能從所有安全性修正程式的相同時間可用性獲得獲益。

### <a name="mui-infrastructure"></a>MUI 基礎結構

從 Windows Vista 開始，MUI Api 可讓開發人員利用自己應用程式的 MUI 機制，而不需要建立自訂邏輯來處理資源和語言管理。

### <a name="language-management"></a>語言管理

提供 UI 語言管理功能的基底 MUI Api 可做為 MUI 基礎結構的一部分。 為了協助管理系統、使用者和應用層級的不同 UI 語言設定，MUI 會在內部將它們合併成單一優先順序的清單。 然後，MUI 會根據此優先順序清單來實行回溯機制，以允許部分當地語系化解決方案，同時為使用者提供適當的（如果不是慣用的）使用者介面語言體驗。

例如，執行西班牙文語言介面套件 (LIP) 安裝在基礎作業系統上的系統可支援下列行為：系統會先嘗試將其資源顯示在加泰羅尼亞文中，如果這些資源不適用於加泰羅尼亞文，則請改為提供使用者西班牙資源。

### <a name="resource-handling"></a>資源處理

從 Windows Vista 開始提供的改良式 MUI 基礎結構，最常見的資源技術已啟用 MUI。 下表提供 Windows Vista 中可用資源處理支援的其他詳細資料。



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
<td>支援的資源類型</td>
<td><ul>
<li>Win32/非受控資源：。DLL/。EXE/。Ocx</li>
<li>Shell 相關的註冊</li>
<li>管理相關資源：事件記錄檔、嵌入式管理單元/SERVICES.MSC 檔案</li>
<li>WMI： MOF/MFL</li>
<li>群組原則： ADMX/ADML</li>
<li>受控 Resources.dll</li>
</ul></td>
</tr>
<tr class="even">
<td>開發工具</td>
<td><ul>
<li>若為 Win32： RC.exe、MUIRCT.exe 和 Visual Studio 2005 和更新版本</li>
</ul></td>
</tr>
<tr class="odd">
<td>有限的資源類型支援</td>
<td><ul>
<li>* .chm 說明檔</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



