---
title: 遠端桌面服務設定類別
description: 遠端桌面服務設定 WMI 提供者提供下列類別。 如下圖所示。
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40784e1e0c9e0387b8d6ff60193639032f7e0cbe5e34c4a8b35aeb32cc37cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000121"
---
# <a name="remote-desktop-services-configuration-classes"></a>遠端桌面服務設定類別

遠端桌面服務設定 WMI 提供者提供下列類別。 如下圖所示。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dd>

代表 managed 系統專案與其定義的設定類別之間的關聯。

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

System 元素階層的基類。

</dd> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dd>

代表一或多個 managed 系統元素的設定相關和指令引數。

</dd> <dt>

[**Win32 \_ 終端機**](win32-terminal.md)
</dt> <dd>

表示終端。

</dd> <dt>

[**Win32 \_ TerminalError**](win32-terminalerror.md)
</dt> <dd>

表示終端機錯誤。

</dd> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dd>

[**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)類別的子類別。 [**Win32 \_TerminalService**](win32-terminalservice.md)代表 [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **Element** 屬性。

</dd> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> <dd>

代表遠端桌面工作階段主機 (RD 工作階段主機) server 的設定。

</dd> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dd>

表示 [**Win32 \_ TerminalService**](win32-terminalservice.md) 類別的實例與特定 [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) 屬性的設定之間的關聯。

</dd> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dd>

表示可以套用至終端機的設定。

</dd> <dt>

[**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dd>

表示終端機與其設定之間的關聯。

</dd> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> <dd>

允許刪除存在於 [**Win32 \_ 終端**](win32-terminal.md) 機上的帳戶，以及修改現有的許可權。

</dd> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> <dd>

定義與連接原則相關的 [**Win32 \_ 終端**](win32-terminal.md) 機類別的設定。

</dd> <dt>

[**Win32 \_ TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

提供探索到的遠端桌面授權伺服器的詳細資料。

</dd> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> <dd>

定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的配置設定，包括初始程式原則。

</dd> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dd>

代表終端機的一般設定，例如加密層級和傳輸通訊協定。

</dd> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> <dd>

定義與用戶端登入相關的 [**Win32 \_ 終端**](win32-terminal.md) 機類別的配置設定。

</dd> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

根據指定的終端通訊協定和傳輸方法，列舉可針對 [**Win32 \_ 終端**](win32-terminal.md)機設定的網路介面卡清單。

</dd> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的各種設定，包括與網路介面卡相關的屬性，以及允許的最大連接數目。

</dd> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> <dd>

包含將新帳戶新增至終端機的方法，以及將預設許可權還原到終端機的方法。

</dd> <dt>

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> <dd>

定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的遠端控制設定。

</dd> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dd>

定義 [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) 類別的遠端桌面連線代理人 (RD 連線代理人) 設定。

</dd> <dt>

[**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)
</dt> <dd>

表示 [**win32 \_ TerminalService**](win32-terminalservice.md) 類別的實例與 [**win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) 類別的實例之間的關聯。

</dd> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> <dd>

定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的設定，例如時間限制以及中斷連線和重新連接動作。

</dd> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> <dd>

定義 RD 工作階段主機伺服器 (IP) 虛擬化設定的網際網路通訊協定。

</dd> <dt>

[**Win32 \_ TSVirtualIPSetting**](win32-tsvirtualipsetting.md)
</dt> <dd>

表示 [**win32 \_ TerminalService**](win32-terminalservice.md) 元素類別和 [**win32 \_ TSVirtualIP**](win32-tsvirtualip.md) 設定類別之間的關聯。

</dd> </dl>

下圖顯示這些類別之間的關聯性。

![支援類別之間的關聯性](images/tswmi.png)

 

 