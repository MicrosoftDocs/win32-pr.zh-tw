---
description: 連接至遠端電腦上的 WMI 命名空間，可能需要您變更 Windows 防火牆、使用者帳戶控制 (UAC) 、DCOM 或通用訊息模型物件管理員的設定， (CIMOM) 。
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: 設定遠端 WMI 連接
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513072"
---
# <a name="setting-up-a-remote-wmi-connection"></a>設定遠端 WMI 連接

連接至遠端電腦上的 WMI 命名空間，可能需要您變更 [Windows 防火牆](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))、 [使用者帳戶控制 (UAC) ](/previous-versions/aa905108(v=msdn.10))、DCOM 或通用訊息模型物件管理員的設定， (CIMOM) 。

本主題將討論下列各節：

-   [Windows 防火牆設定](#windows-firewall-settings)
-   [使用者帳戶控制設定](#user-account-control-settings)
-   [DCOM 設定](#dcom-settings)
-   [CIMOM 設定](#cimom-settings)
-   [相關主題](#related-topics)

## <a name="windows-firewall-settings"></a>Windows 防火牆設定

Windows 防火牆設定的 WMI 設定只會啟用 WMI 連接，而不是其他 DCOM 應用程式。

您必須在遠端目的電腦上的適用于 WMI 的防火牆中設定例外狀況。 WMI 的例外狀況可讓 WMI 接收遠端連線，以及 Unsecapp.exe 的非同步回呼。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

如果用戶端應用程式建立自己的接收，則必須明確地將該接收器新增至防火牆例外狀況，以允許回呼成功。

WMI 的例外狀況也適用于 WMI 以固定通訊埠啟動時，使用 **winmgmt/standalonehost** 命令。 如需詳細資訊，請參閱 [設定 WMI 的固定通訊埠](setting-up-a-fixed-port-for-wmi.md)。

您可以透過 Windows 防火牆 UI 啟用或停用 WMI 流量。

**使用防火牆 UI 啟用或停用 WMI 流量**

1.  在 [ **主控台** 中，按一下 [ **安全性** ]，然後按一下 [ **Windows 防火牆**]。
2.  按一下 [ **變更設定** ]，然後按一下 [ **例外** ] 索引標籤。
3.  在 [例外狀況] 視窗中，選取 [ **wmi) 的 Windows Management Instrumentation (** ] 核取方塊，以啟用通過防火牆的 wmi 流量。 若要停用 WMI 流量，請清除此核取方塊。

您可以在命令提示字元中，透過防火牆啟用或停用 WMI 流量。

**若要在命令提示字元使用 WMI 規則群組啟用或停用 WMI 流量**

-   在命令提示字元中使用下列命令。 輸入下列各項，以啟用通過防火牆的 WMI 流量。

    **netsh advfirewall firewall set rule group = "windows management instrumentation (wmi) " new enable = yes**

    輸入下列命令，以停用透過防火牆的 WMI 流量。

    **netsh advfirewall firewall set rule group = "windows management instrumentation (wmi) " new enable = no**

您也可以針對每個 DCOM、WMI 服務和接收器使用個別命令，而不是使用 [單一 WMI 規則群組] 命令。

**針對 DCOM、WMI、回呼接收和連出連線使用不同的規則來啟用 WMI 流量**

1.  若要建立 DCOM 通訊埠135的防火牆例外，請使用下列命令。

    **netsh advfirewall firewall add rule dir = in name = "DCOM" program =% systemroot% \\ system32 \\svchost.exe service = rpcss action = allow PROTOCOL = TCP localport = 135**

2.  若要建立 WMI 服務的防火牆例外狀況，請使用下列命令。

    **netsh advfirewall firewall add rule dir = in name = "WMI" 程式 =% systemroot% \\ system32 \\svchost.exe service = winmgmt action = allow PROTOCOL = TCP localport = any**

3.  若要針對接收遠端電腦回呼的接收建立防火牆例外，請使用下列命令。

    **netsh advfirewall firewall add rule dir = in name = "Unsecapp.exe" program =% systemroot% \\ system32 \\ wbem \\unsecapp.exe action = allow**

4.  若要針對本機電腦與本機電腦進行通訊的遠端電腦，建立外寄連線的防火牆例外，請使用下列命令。

    **netsh advfirewall firewall add rule dir = out name = "WMI \_ out" 程式 =% systemroot% \\ system32 \\svchost.exe service = winmgmt action = ALLOW protocol = TCP localport = any**

若要分別停用防火牆例外狀況，請使用下列命令。

**使用 DCOM、WMI、回呼接收和傳出連線的個別規則來停用 WMI 流量**

1.  停用 DCOM 例外狀況。

    **netsh advfirewall firewall delete rule name = "DCOM"**

2.  停用 WMI 服務例外狀況。

    **netsh advfirewall firewall delete rule name = "WMI"**

3.  停用接收例外狀況。

    **netsh advfirewall firewall delete rule name = "Unsecapp.exe"**

4.  停用外寄例外狀況。

    **netsh advfirewall firewall delete rule name = "WMI \_ OUT"**

## <a name="user-account-control-settings"></a>使用者帳戶控制設定

使用者帳戶控制 (UAC) 存取權杖篩選可能會影響 WMI 命名空間中允許的作業或傳回的資料。 在 UAC 下，本機 Administrators 群組中的所有帳戶都是以標準使用者 [*存取權杖*](/windows/desktop/SecGloss/a-gly)（也稱為 UAC 存取權杖篩選）來執行。 系統管理員帳戶可以使用較高的許可權（「以系統管理員身分執行」）來執行腳本。

當您未連線到內建的系統管理員帳戶時，UAC 會根據兩部電腦是否位於網域或工作組中，以不同的方式影響遠端電腦的連線。 如需 UAC 和遠端連線的詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。

## <a name="dcom-settings"></a>DCOM 設定

如需 DCOM 設定的詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。 不過，UAC 會影響非網域使用者帳戶的連接。 如果您使用遠端電腦的 [本機系統管理員] 群組中包含的非網域使用者帳戶連接到遠端電腦，則必須明確授與遠端 DCOM 存取、啟動及啟動帳戶的許可權。

## <a name="cimom-settings"></a>CIMOM 設定

如果遠端連線是在沒有信任關係的電腦之間，則必須更新 CIMOM 設定;否則，非同步連接將會失敗。 針對相同網域或受信任網域中的電腦，不應修改此設定。

您必須修改下列登錄專案，才能允許匿名回呼：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

如果 **AllowAnonymousCallback** 值設定為0，則 WMI 服務會防止用戶端匿名回呼。 如果值設定為1，則 WMI 服務允許對用戶端進行匿名回呼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
