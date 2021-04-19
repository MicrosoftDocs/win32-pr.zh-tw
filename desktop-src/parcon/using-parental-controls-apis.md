---
description: 使用家長監護 Api
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: 使用家長監護 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989386"
---
# <a name="using-parental-controls-apis"></a>使用家長監護 Api

## <a name="api-selection"></a>API 選取專案

如「總覽」一節所述，開發牽涉到使用最多三個 Api：

-   基本設定存取：家長能控制 Wpcapi 中定義的最低相容性 COM API (合規性 API) ，以便簡單存取家長監護的主要控制項狀態子集。
-   完整設定寫入/讀取權限：只有在 ISV 需要修改設定時，才需要使用一小部分的 WMI COM API 來進行完整存取。 使用 API 的主要原因是新增 UI 擴充性連結、取代 Web 內容篩選，或新增至全電腦的 HTTP 應用程式或 URL 篩選豁免清單。 由於 WMI 家長監護控制項命名空間使用方式提供了基礎設定存放區的原始存取權，因此 Isv 應該在解讀其他設定的相依性時，小心地解讀個別設定的狀態。 因此，建議使用合規性 API 來讀取該 API 所公開之所有值的狀態。
-   記錄： Windows Vista 事件追蹤和報告系統 API (也稱為 ETW) ，可將活動事件發佈到家長監護記錄中，以及 WpcEvent 中定義的事件描述元和陣列列舉。

所有 Api 都可作為標準使用者來呼叫。 若為記錄，任何使用者都可能發生來源記錄事件。 如果呼叫端沒有系統管理員許可權，呼叫以抓取或變更其他使用者的設定將會失敗。 換句話說，標準使用者只能存取自己的設定，而且只可供閱讀。

這些章節將進一步討論設定和記錄 API 使用量：

-   [使用家長監護設定 Api](using-parental-controls-settings-apis.md)
-   [使用適用于家長監護的記錄 Api](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a>開發環境

開發家長監護需要存取三個標頭檔： Wpc .h、WpcApi .h 和 WpcEvent .h。 Wpc 是一種收集器，其中包含公用合規性 API 和事件標頭的設定，因此您可以在應用程式程式碼中包含 Wpc。

WMI API 的讀取/寫入權限是由 Wpcsprov. mof 檔案所指定。 此檔案會安裝到 Windows System32 目錄下的 WBEM 子目錄。

Microsoft Windows 軟體開發套件 (SDK) 包含範例程式碼，以強化此處顯示的範例程式碼，並提供簡單的命令列導向工具來進行 API 探索或整合測試。

 

 



