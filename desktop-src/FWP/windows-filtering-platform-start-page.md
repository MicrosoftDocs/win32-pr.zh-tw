---
title: Windows 篩選平台
description: Windows篩選 Platform (WFP) 是一組 API 和系統服務，可提供建立網路篩選應用程式的平臺。
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Windows 篩選平台
- Windows篩選平臺起始頁，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c1f0e412426dd2bae7e5861d3b328d4e285c303aef046970e725a02965b974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766488"
---
# <a name="windows-filtering-platform"></a>Windows 篩選平台

## <a name="purpose"></a>目的

Windows篩選 Platform (WFP) 是一組 API 和系統服務，可提供建立網路篩選應用程式的平臺。 WFP API 可讓開發人員撰寫程式碼，該程式碼會與在作業系統網路堆疊的數個層級上發生的封包處理進行互動。 您可以篩選網路資料，也可以在到達目的地之前加以修改。

藉由提供更簡單的開發平臺，WFP 是設計來取代先前的封包篩選技術，例如傳輸驅動程式介面 (TDI) 篩選器、網路驅動程式介面規格 (NDIS) 篩選器，以及 (LSP) 的 Winsock 分層服務提供者。 從 Windows Server 2008 和 Windows Vista 開始，防火牆攔截和篩選器攔截器驅動程式無法使用;使用這些驅動程式的應用程式應該改用 WFP。

使用 WFP API，開發人員可以執行防火牆、入侵偵測系統、防毒程式、網路監視工具和家長監護。 WFP 與整合，並根據應用程式使用通訊端 API (以應用程式為基礎的原則) ，來提供防火牆功能的支援，例如已驗證的通訊和動態防火牆設定。 WFP 也提供 IPsec 原則管理、變更通知、網路診斷和具狀態篩選的基礎結構。

Windows篩選平臺是開發平臺，而不是防火牆本身。 Windows Vista、Windows Server 2008 和更新版本的作業系統中內建的防火牆應用程式，Windows 具有 Advanced Security (WFAS) 的防火牆會使用 WFP 來執行。 因此，使用 WFP API 或 [WFAS api](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) 開發的應用程式會使用內建于 wfp 的一般篩選仲裁邏輯。

WFP API 是由使用者模式 API 和核心模式 API 所組成。 本節提供整個 WFP 的總覽，並詳細說明 WFP API 的使用者模式部分。 如需核心模式 WFP API 的詳細說明，請參閱[Windows 驅動程式套件](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)線上說明。

## <a name="developer-audience"></a>開發人員對象

Windows 篩選平台 API 是設計來供程式設計人員使用 C/c + + 開發軟體。 程式設計人員應該熟悉網路概念，以及使用使用者模式和核心模式元件的系統設計。

## <a name="run-time-requirements"></a>執行階段需求求

執行 Windows Vista 和更新版本的用戶端，以及在執行 Windows Server 2008 和更新版本的伺服器上，都支援 Windows 篩選平台。 如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。





 

## <a name="in-this-section"></a>本節內容



| 主題                                                                                               | 描述                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Windows 篩選平台的新功能](what-s-new-in-windows-filtering-platform.md)<br/> | Windows 篩選平台中新功能和 api 的資訊。<br/>                    |
| [關於 Windows 篩選平台](about-windows-filtering-platform.md)<br/>                 | Windows 篩選平台的總覽。<br/>                                             |
| [使用 Windows 篩選平台](using-windows-filtering-platform.md)<br/>                 | 使用 Windows 篩選平台 API 的範例程式碼。 <br/>                                |
| [Windows篩選平臺 API 參考](fwp-reference.md)<br/>                            | Windows 篩選平台函數、結構和常數的檔。<br/> |



 

## <a name="additional-resources"></a>其他資源

若要詢問問題並取得有關使用 WFP API 的討論，請造訪[Windows 篩選平台論壇](https://social.msdn.microsoft.com/forums/wfp/threads/)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心模式 Windows 篩選平台 API-設計指南](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[核心模式 Windows 篩選平台 API-參考](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[具有進階安全性的 Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[WFP 診斷可延伸 Helper 類別](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Winsock 安全通訊端擴充功能](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

