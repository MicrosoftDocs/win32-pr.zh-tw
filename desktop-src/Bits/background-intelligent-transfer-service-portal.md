---
title: 背景智慧型傳送服務
description: 背景智慧型傳送服務 (BITS) 會在用戶端和伺服器之間傳輸檔案 (下載或上傳)，並提供有關傳輸的進度資訊。
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- 背景智慧型傳送服務
- 背景智慧型傳送服務，起始頁
- 'BITS (查看背景智慧型傳送服務) '
- 下載檔案位
- 背景檔案傳輸位元組
- 上傳檔案位
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 66bc9af5231454ef63d8c74f9e500baaeb7c8cec9dbdd694943a3809da4a391d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588728"
---
# <a name="background-intelligent-transfer-service"></a>背景智慧型傳送服務

## <a name="purpose"></a>目的

程式設計師和系統管理員會使用背景智慧型傳送服務 (位) ，從檔案下載檔案或將檔案上傳至 HTTP 網頁伺服器和 SMB 檔案共用。 BITS 會考慮傳送的費用，以及網路使用量，如此一來，使用者的前景工作就越不會受到影響。 BITS 也會處理網路 interuptions、暫停和自動繼續傳輸，即使在重新開機後也一樣。 BITS 包含用於建立和管理傳輸以及 BitsAdmin 命令列公用程式的 PowerShell Cmdlet。

> [!Note]  
> Windows 可以使用 BITS 將更新下載至您的本機系統。 如果您是使用者搜尋如何針對 BITS 安裝進行疑難排解的方法，請參閱[修正 Windows Update 問題](https://support.microsoft.com/help/10164/fix-windows-update-errors)。 
 

## <a name="where-applicable"></a>適用時

針對需要下列動作的應用程式使用 BITS：

-   從檔案下載或上傳至 HTTP 或 REST web 伺服器或 SMB 檔案伺服器。
-   在網路中斷連線並重新啟動電腦之後，自動繼續檔案傳輸。
-   保留其他網路應用程式的回應性。
-   請注意網路成本，例如漫遊網路
-   選擇性地使用 [BranchCache](/windows-server/networking/branchcache/branchcache) 將廣域網路) 流量優化 (

## <a name="developer-audience"></a>開發人員對象

BITS 是針對 C 和 c + + 開發人員所設計的 COM 介面，也可供 .NET 開發人員使用。 UWP 開發人員應該使用[Windows。Windows.networking.backgroundtransfer.contentprefetcher](/uwp/api/Windows.Networking.BackgroundTransfer) API，而不是 BITS api。

## <a name="bits-versions"></a>BITS 版本

如需舊版作業系統的完整版本歷程記錄和資訊，請參閱 [新功能](what-s-new.md)。


## <a name="in-this-section"></a>本節內容



| 主題                                                           | 描述                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 BITS](about-bits.md)<br/>                         | 關於位的一般資訊。<br/>                                                                                                                                      |
| [使用 BITS](using-bits.md)<br/>                         | 開發在用戶端與伺服器之間傳輸檔案之 BITS 用戶端的程式指南。<br/>                                                                        |
| [BITS 參考](bits-reference.md)<br/>                 | BITS 程式設計介面的參考資訊。 也包含有關範例、工具、上傳作業的伺服器設定，以及上傳通訊協定的資訊。<br/> |
| [最佳作法](best-practices-when-using-bits.md)<br/> | 設計使用 BITS 的應用程式時應考慮的資訊。<br/>                                                                                                |



 

## <a name="additional-resources"></a>其他資源

以下是其他資源。


|    資源         |    描述                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| .NET 參考 DLL   | 如需使用參考 Dll 從 .NET 使用 BITS 的詳細資訊，請參閱 [使用參考 dll 從 .Net 呼叫位](/windows/desktop/Bits/bits-dot-net)      |
| .NET 包裝函式   | 若是其他適用于 BITS 的 .NET 包裝函式，您可以在 [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) 中搜尋以 bits 標記標記的專案。        |



 

 

