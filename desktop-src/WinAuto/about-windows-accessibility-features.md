---
title: Windows 協助工具功能
description: Windows 協助工具支援 Windows 開發人員的兩種功能類別： Win32 Api 和使用者設定。
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd92ed8594d711ae9b744dc7f4a2622e8cb3d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023703"
---
# <a name="windows-accessibility-features"></a>Windows 協助工具功能

Windows 協助工具支援兩種功能，可協助 Windows 開發人員設計可存取的應用程式、輔助技術開發人員建立工具，例如螢幕閱讀程式和放大鏡，而軟體測試工程師會建立自動化腳本來測試 Windows 應用程式。

## <a name="settings"></a>設定

有兩種類型的設定可供使用者 (透過主控台) 中也會公開給開發人員的輕鬆存取中心：

- [協助工具參數](accessibility-parameters.md)。 設定時，這些參數表示應用程式應該變更其預設行為。 應用程式可以檢查協助工具參數的狀態，以判斷使用者是否想要以應用程式特定的方式提供特殊行為。 例如，「聲音聲」參數表示通常使用音效來傳達重要資訊的應用程式，也應該以視覺化方式提供資訊。
- [內建的協助工具功能](built-in-accessibility-features.md)。 這些功能已內建在系統中，或提供為系統的擴充功能。 它們會影響使用者提供鍵盤和滑鼠輸入至電腦的方式。 啟用時，不論正在執行哪些應用程式，都可以使用其功能。 例如，鍵盤篩選器可讓有行動的使用者更輕鬆地輸入按鍵組合（例如 CTRL + ALT + DEL）。

每個協助工具參數和每個內建的協助工具功能都會對應到可使用 [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式進行設定或查詢的系統參數。

## <a name="win32-apis"></a>Win32 API

Win32 Api 提供協助工具和自動化功能，可協助開發人員建立應用程式和 UI 架構、輔助技術廠商建立工具、測試人員確保品質的執行，以及殘障人士使用他們的電腦和裝置。

## <a name="related-topics"></a>相關主題

[輔助技術的安全性考慮](uiauto-securityoverview.md)