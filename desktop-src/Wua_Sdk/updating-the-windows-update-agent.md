---
description: Windows Update 代理程式 (WUA) 在連線到 Windows Server Update Services (WSUS) 伺服器或 Windows Update 時，自動自行更新。
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: 正在更新 Windows Update 代理程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fe439b1bea377e2699f6fe5714b208ac5d951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970444"
---
# <a name="updating-windows-update-agent"></a>正在更新 Windows Update 代理程式

根據裝置上執行的 Windows 版本而定，Windows Update 代理程式 (WUA) 會透過各種方式自行更新。 舊版 WUA 可能無法連線到目前的更新服務，可能無法與所有更新相容，而且可能不支援所有記載的 Api。 以下說明如何確保 WUA 已完全更新且相容。

**從 Windows 7 和 Windows Server 2008 R2 開始的 Windows 版本**

Windows Update Agent (WUA) 更新會包含在透過 Windows Update 或 Windows Server Update Services (WSUS) 發佈的 Windows 定期更新中。 在這些 Windows 版本上，您不需要採取任何特殊步驟來更新 WUA。

**在 Windows 7 和 Windows Server 2008 R2 之前的 Windows 版本**

當自動更新連接到 Windows Update 或 WSUS 時，WUA 會自動自行更新。

如果自動更新尚未成功執行，則執行這些 Windows 版本的裝置可能會執行不支援所有記載之 Api 的舊版 WUA。 如果您在使用 WUA API 來執行掃描、下載或安裝時收到 WU_E_SELFUPDATE_REQUIRED 結果，此錯誤表示安裝的 WUA 版本太舊，無法連接到目前的 Windows Update 服務。 您無法使用標準 WUA Api 來更新這些作業系統上的 WUA。 

使用者可以藉由開啟 Windows Update 控制台、選取 [檢查更新]，然後接受顯示的自動更新，來手動將 WUA 更新為最新版本。 或者，您可以用程式設計的方式更新 WUA。

**以程式設計方式在 Windows 7 和 Windows Server 2008 R2 之前的 Windows 版本上更新 WUA**

1.  使用 [WinHTTP](../winhttp/winhttp-start-page.md) api 下載 [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab)。
2.  使用 [密碼編譯功能](../seccrypto/cryptography-functions.md) 來確認下載的 [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) 複本是否有 Microsoft 的數位簽章。 如果您無法驗證數位簽章，請停止。
3.  使用檔案 [解壓縮介面](../devnotes/cabinet-api-functions.md) api 從 [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab)解壓縮 XML 檔案。
4.  使用 Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))) api 來載入 XML 檔案，並找出電腦架構的 WURedist/StandaloneRedist/架構節點。 例如，針對 x86，找出 [WURedist/StandaloneRedist]/[架構] 節點，並使用 [x86] 的 [ **名稱** ] 屬性。
5.  呼叫 [**IWindowsUpdateAgentInfo：： GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) 來判斷 WUA 的目前版本。 如果 **IWindowsUpdateAgentInfo：： GetInfo** 傳回的版本號碼至少與您所在之架構節點中的 **clientVersion** 屬性高，請停止。
6.  使用 [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) api 從您找到的 [架構] 節點讀取 **downloadUrl** 屬性。 **downloadUrl** 可為您提供適用于電腦架構之 WUA 安裝程式的下載 URL。
7.  使用 [WinHTTP](../winhttp/winhttp-start-page.md) api 下載適當的安裝程式。
8.  使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數或類似的 API 來執行下載的安裝程式。

 

 
