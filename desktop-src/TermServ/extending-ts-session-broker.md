---
title: 擴充 Terminal Services Session Broker
description: 您可以擴充 TS \ 160;使用 IWTSSBPlugin COM 介面的會話代理程式。
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c859320c11a128ab01a719d17abd9927ea96f312e0aa3df5f0be76dcc0226b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737688"
---
# <a name="extending-terminal-services-session-broker"></a>擴充 Terminal Services Session Broker

終端機服務會話代理人 (「TS 會話代理人」) 判斷起始連接的使用者是否已開啟會話。 如果是，TS 會話代理人會將連入連線路由傳送至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器與現有的會話。 如果不是，則 TS 會話代理人會將連入連線以最少的會話路由傳送至 RD 工作階段主機伺服器。

您可以使用 [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM 介面擴充 TS 會話代理人。 您可以使用此介面來管理 RD 工作階段主機伺服器的連線，以及任何類型的遠端桌面通訊協定 (RDP) 連線，例如，連線至在 Windows Server 2008 hyper-v 虛擬機器主機上執行 Enterprise Vista (集中式桌面) VECD Windows 的來賓虛擬機器。

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)介面提供幾項優點：

-   不需要在用戶端或 RD 工作階段主機伺服器上安裝代理程式。
-   外掛程式可以與其他遠端桌面服務角色服務緊密互動，例如遠端桌面閘道 (RD 閘道) ，以及依賴 TS 會話代理人有關會話和電腦狀態的資訊。
-   您可以使用外掛程式來管理支援 RDP 5.2 或更新版本之用戶端或伺服器裝置的連線。
-   您可以使用外掛程式來啟用 Windows Vista Enterprise 集中式桌面解決方案。

當您執行此介面的方法時，請記住下列幾點：

-   TS 會話代理人可能會從多個執行緒呼叫這個 COM 物件的方法。
-   如果任何呼叫的方法不會立即和成功傳回，TS 會話代理人就不會再呼叫該外掛程式並還原為其原生負載平衡邏輯。 若要繼續呼叫外掛程式，您必須重新開機終端機服務會話代理人服務。
-   您必須使用 Regsvr32.exe，將外掛程式註冊為整個系統的 COM 物件。 因為終端機服務會話代理人服務是在 "NetworkService" 帳戶下執行，所以您必須使用 Dcomcnfg.exe 為 "NetworkService" 帳戶提供必要的啟動、啟用和存取權限。 終端機服務會話代理人服務會在下列登錄子機碼中尋找代表外掛程式的 COM 物件 CLSID：

    **HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **參數** \\ **ExtensibilityPluginCLSID**

如需 Dcomcnfg.exe 的詳細資訊，請參閱 [使用 DCOMCNFG 啟用 COM 安全性](/windows/desktop/com/enabling-com-security-using-dcomcnfg)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 