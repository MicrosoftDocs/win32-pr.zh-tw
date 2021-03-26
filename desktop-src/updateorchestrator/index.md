---
title: 更新 Orchestrator API
description: UpdateOrchestrator 會排程您的自動軟體更新，並考慮使用者的影響。
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: a172cccdc56d2c645bb4e7d048066ca34aea07ba
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "103853179"
---
# <a name="updateorchestrator-api"></a>UpdateOrchestrator API

**UpdateOrchestrator** 會排程您的自動軟體更新，並考慮使用者的影響。 此 API 可讓您排程自動下載和安裝，以及它們的需求，以在最接近使用者的影響的最佳時間執行更新。 這些功能特別能以受限或較慢的運算資源，以較低的效能系統來獲益。

Windows 19H1 包含第一代解決方案，適用于 OS 更新所採用的自動軟體更新使用案例和儲存應用程式更新，並公開此 API 的初始「有限存取」版本，適用于一組更新程式的「使用者模式」應用程式，如下所述。

## <a name="features"></a>功能

- 以動態方式註冊軟體更新程式
 
- 在優化期間叫用已註冊的軟體更新程式，例如在使用者不存在的情況下，更新「使用者模式應用程式」。
    - 包含在 AC 電源上「保持喚醒」的功能，可進一步降低使用者的影響。

- 在只叫用受信任的協力廠商註冊軟體的信任模型上運作更新程式
    - 將 UpdateOrchestrator 公開給任何和所有呼叫端（例如，在使用者不存在時更新 BIOS 固件或驅動程式）時，會有相當大的風險。  UpdateOrchestrator 包含可減輕這些風險的信任模型。

## <a name="developer-audience"></a>開發人員讀者

> [!IMPORTANT]
> UpdateOrchestrator API 目前為有限的 [存取功能](/uwp/api/windows.applicationmodel.limitedaccessfeatures)。 此 API 將會在未來的版本中公開提供。

如果您已經有適用于 Win32 「使用者模式」應用程式的背景軟體更新程式，例如適用于 Acrobat Reader 或閥門串流的 Adobe 更新程式，請使用 UpdateOrchestrator API。 UWP/Store 應用程式不需要此介面，因為 Microsoft Store 已經利用此功能來進行軟體更新。

為了提供最佳的客戶體驗，此初始 API 版本的範圍是一組符合下列準則的已註冊更新程式：

- 僅限「使用者模式」應用程式的更新
- 不涉及 BIOS/固件/裝置或軟體驅動程式
    - 更新未通過一般品質準則的 BIOS、固件或裝置/軟體驅動程式會造成重大風險，特別是當使用者不存在時。 
- 參與此 API 的使用方式，需要能夠擔保您的背景軟體更新程式在使用者系統上透過審核所下載及安裝的所有內容。 

此 API 可能會在公開發行之前大幅修改。   在開發 UpdateOrchestrator API 時，此初始版本為限制存取功能，僅適用于目前符合上述準則的更新程式。

我們的目標是要改善此 API 的功能，並減少在 Windows 上更新程式多個自動軟體的影響。 我們會透過這 [**份簡短問卷**](https://aka.ms/UOAPISurvey) 來感謝您的輸入，以協助我們瞭解 UpdateOrchestrator API 如何能更妥善地滿足您的開發人員需求。

