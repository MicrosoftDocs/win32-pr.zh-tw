---
title: 使用遠端桌面服務
description: 如何在遠端桌面服務環境中進行程式設計，以及如何使用遠端桌面網頁連線將先前稱為終端機服務) 技術的遠端桌面服務 (延伸至網路。
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d0af90aef8eed3c8b9dc397f86cb6940a79e8e399af201ff854cbfaba3ff3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868768"
---
# <a name="using-remote-desktop-services"></a>使用遠端桌面服務

下列各節說明如何在遠端桌面服務環境中進行程式設計，以及如何使用遠端桌面網頁連線將先前稱為終端機服務) 技術的遠端桌面服務 (延伸至 web。 如果您要尋找遠端桌面連線的使用者資訊，請參閱[使用遠端桌面連線連線到另一部電腦](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)。

> [!Note]  
> 本主題適用于軟體發展人員。

 

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[偵測是否已安裝遠端桌面服務角色](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

c # 程式碼範例，示範如果遠端桌面服務伺服器角色已安裝且正在執行，則會傳回 **True** 的方法，否則從 Windows server 2008 開始，則為 **false** 。

</dd> <dt>

[擴充 Terminal Services Session Broker](extending-ts-session-broker.md)
</dt> <dd>

您可以使用 [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM 介面擴充 TS 會話代理人。

</dd> <dt>

[執行自訂音訊端點列舉值](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

從 Windows Server 2008 R2 開始，您可以在遠端桌面通訊協定提供者中執行自訂的遠端音訊端點枚舉器。

</dd> <dt>

[會話的名字](session-monikers.md)
</dt> <dd>

分散式 COM (DCOM) 使用系統提供的會話標記，啟用每個會話的物件啟用。

</dd> <dt>

[使用遠端桌面服務使用者設定的 ADSI 擴充功能](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

您可以使用 Active Directory 服務介面所執行的方法來管理遠端桌面服務特定的使用者屬性， (ADSI) 延伸模組，該擴充功能會與動態連結程式庫 Tsuserex.dll 一起封裝。

</dd> <dt>

[使用遠端桌面服務 API](using-the-terminal-services-api.md)
</dt> <dd>

說明如何使用遠端桌面服務 API，讓應用程式在遠端桌面服務環境中執行工作。

</dd> <dt>

[使用遠端桌面虛擬化 API](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

開發人員可以使用此 API 來自訂遠端桌面連線代理人 (RD 連線代理人) 用來判斷連入用戶端連線最佳目的地的邏輯。

</dd> <dt>

[自訂 VDI 解決方案的 WSDL 介面](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

開發人員可以建立自訂 web 服務，以管理 (VDI) 解決方案的虛擬桌面基礎結構。

</dd> </dl>

如需詳細資訊，請參閱 [遠端桌面服務程式設計指導方針](terminal-services-programming-guidelines.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[終端機服務現在遠端桌面服務](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[偵測遠端桌面服務環境](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




