---
description: Internet Explorer 8-資料執行防止/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-資料執行防止/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1f969aa2e934f36142995150b6484dad2fa5067f6cbb5ab3a947055af375ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998888"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8-資料執行防止/NX

## <a name="affected-platforms"></a>受影響的平臺

 **客戶** 端-Windows XP、Windows Vista、Windows 7  
**伺服器**-Windows server 2003、Windows server 2008、Windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 將在具有最新 service pack 的作業系統上執行時，啟用 DEP/NX 保護。 WindowsXP SP3、Windows Server 2003 SP3、Windows Vista SP1 和 Windows Server 2008 都預設會在 Internet Explorer 8 中啟用 DEP/NX。

 

## <a name="feature-impact"></a>功能影響

**嚴重性** -中  
**頻率** -低  

> [!Note]  
> 一般來說，在 Internet Explorer 中執行且與 DEP/NX 不相容的任何應用程式都會在啟動時損毀，且無法運作。 如果安裝了不相容于 DEP/NX 的附加元件，Internet Explorer 可能會在啟動時損毀。

 

## <a name="description"></a>描述

DEP/NX 是一種安全性功能，可協助減輕記憶體相關弱點。 從 Internet Explorer 8，所有 Internet Explorer 進程預設都會啟用 DEP/NX 功能。

## <a name="manifestation-of-impact"></a>影響的表現

Windows 核心會監視程式的執行。 如果核心偵測到嘗試從未標記為可執行檔的記憶體頁面執行程式碼，則核心會停止執行程式，並產生「損毀」。 這是一項安全性措施，可協助確保記憶體相關弱點 (例如，應用程式中的緩衝區溢位) 無法被惡意探索，以執行任意程式碼。

## <a name="end-user-mitigation"></a>End-User 風險降低

-   安裝較新版本的附加元件或與 DEP/NX 相容的 framework。
-   以系統管理員的身分執行 Internet Explorer，然後在 [**網際網路選項**] 的 [選項] 索引標籤上，使用 [**啟用記憶體保護] 來防止線上攻擊** 核取方塊停用 DEP/NX  /   。

## <a name="developer-solution"></a>開發人員解決方案

使用與 DEP 相容的最新 framework 版本來編譯應用程式。

## <a name="leveraging-feature-capabilities"></a>運用功能功能

-   使用/NXCOMPAT 連結器選項來指出 DEP/NX 相容性
-   將您的程式碼加入其他可用的防禦機制，例如 stack 防禦 (/GS) 、安全例外狀況處理 (/SafeSEH) 和 ASLR (/DynamicBase) 

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

-   使用 Windows Vista SP1 或更新版本上最新發行的 Internet Explorer 版本，在啟用 DEP/NX 的情況下測試您的程式碼。
-   啟用 DEP/NX 選項之後，請在 Windows Vista 上使用 Internet Explorer 7 進行測試。 若要啟用 Internet Explorer 7 的 DEP/NX，請以系統管理員身分執行 Internet Explorer，然後在 [工具 > 的 [網際網路選項] > [Advanced] 索引標籤中，設定適當的核取方塊。
-   使用應用程式相容性工具組所提供的 Internet Explorer 相容性測試控管 (IECTT)  (ACT) 找出因 DEP/NX 變更而產生的任何潛在問題。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [Internet Explorer 8 安全性第 I 部： DEP/NX 記憶體保護](/archive/blogs/ie/)
-   [資料執行防止](../memory/data-execution-prevention.md)
-   [已將新的 NX api 新增至 Windows Vista SP1、Windows XP SP3 和 Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [應用程式相容性工具組下載](/windows-hardware/get-started/adk-install)
-   [已知 Internet Explorer 安全性功能問題](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
