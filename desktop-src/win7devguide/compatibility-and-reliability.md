---
title: 相容性和可靠性
description: Windows 7 的設計目的是要在 Windows Vista 的相同硬體上執行，並與適用于 Windows Vista 的應用程式和設備磁碟機相容。
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e9686c732c94b4b99408d0fd6e24f84079ee9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967279"
---
# <a name="compatibility-and-reliability"></a>相容性和可靠性

Windows 7 的設計目的是要在 Windows Vista 的相同硬體上執行，並與適用于 Windows Vista 的應用程式和設備磁碟機相容。

Windows 7 是目前最可靠的 Windows 版本。 Windows 7 是以改良的技術基礎來設計，可讓使用者可靠地啟動、關機或休眠電腦，而不必擔心遺失寶貴的工作。 此外，Windows 7 還可讓您比以往更輕鬆地將資料備份和還原到網路磁碟機機或數位攝影機 (Dvd) 。 Windows 7 也可以改善列印可靠性和效能。  (請參閱 [Windows 7 應用程式品質操作手冊](../win7appqual/windows-7-application-quality-cookbook.md)。 ) 

## <a name="applications"></a>應用程式

為了確保相容性，Windows 7 的設計與軟體廠商和電腦製造商之間的合作關係更加密切。 早期參與已讓 Microsoft 建立最廣泛使用之應用程式的完整清單。 自動化測試週期可確保在開發週期初期偵測到相容性問題並加以修正。  (參閱 [Windows 應用程式相容性](/windows/apps/desktop/)。 ) 

## <a name="drivers"></a>驅動程式

Windows 驅動程式套件 (WDK) 7.0.0 版提供開發人員建立 Windows 品質驅動程式所需的組建環境、工具、檔和範例。 WDK 7.0.0 支援靜態原始程式碼分析，使用 PREfast 來偵測某些 C 和 c + + 程式碼錯誤類別。 PREfast 包含特殊的驅動程式元件，稱為驅動程式的 PREfast (PFD) ，可偵測核心模式驅動程式程式碼中的錯誤。 此外，您還可以針對 PFD 支援的所有核心標頭檔加上批註，以增強 WDK。 已新增新的範例驅動程式來示範新的技術，而且檔已擴充。

Windows 7 支援廣泛的軟體和硬體產品，其設計目的是要與平臺完美整合。 針對 Windows Vista 所建立的驅動程式應該不需要更新，就能在 Windows 7 中正確執行。  (參閱 [Windows 驅動程式套件](/windows-hardware/drivers/)。 ) 

## <a name="devices"></a>裝置

Windows 7 針對各種應用程式和裝置提供彈性、健全的支援，包括音樂播放機、存放裝置、行動電話和其他類型的連線裝置。 這些裝置的自動測試是用來確保在開發週期初期修正相容性問題。  (參閱 [Windows 裝置類別基本](https://www.microsoft.com/whdc/device/default.mspx)概念。 ) 

## <a name="reliability-analysis-component"></a>可靠性分析元件

可靠性分析元件是一個內建的代理程式，可提供有關系統使用量和可靠性的詳細客戶體驗資訊。 這項資訊是透過 Windows Management Instrumentation (WMI) 介面公開，讓可供便攜讀取器系統取用。 藉由透過 WMI 介面公開可靠性分析元件，開發人員可以監視及分析應用程式，進而提高可靠性和效能。

Windows 7 會使用內建的可靠性分析元件來計算可靠性索引，以提供您的整體系統使用狀況和隨時間變化的穩定性資訊。 可靠性分析元件也會追蹤系統的任何重要變更，這些變更可能會影響穩定性，例如 Windows update 和應用程式安裝。 您可以使用 [可靠性監視器] 嵌入式管理單元來查看系統的可靠性指數中與這些可能不穩定事件相關的趨勢，讓您輕鬆地直接追蹤對特定事件的可靠性變更。  (參閱 [MountVHD](/previous-versions/windows/desktop/msvs/mountvhd)函式。 ) 

 

 