---
description: " (UAC) 的使用者帳戶控制會影響命令列工具所傳回的 WMI 資料、遠端存取，以及腳本必須如何執行。 如需 UAC 的詳細資訊，請參閱使用使用者帳戶控制開始使用。"
ms.assetid: f6840aaa-834b-42c8-b641-01c570078fcb
ms.tgt_platform: multiple
title: 使用者帳戶控制和 WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39d48abcffa537d886397092c6d4a7b558825021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984990"
---
# <a name="user-account-control-and-wmi"></a>使用者帳戶控制和 WMI

 (UAC) 的使用者帳戶控制會影響命令列工具所傳回的 WMI 資料、遠端存取，以及腳本必須如何執行。 如需 UAC 的詳細資訊，請參閱 [使用使用者帳戶控制開始使用](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)。

下列各節說明 UAC 功能：

-   [使用者帳戶控制](#user-account-control-and-wmi)
-   [執行 WMI Command-Line 工具所需的帳戶](#account-needed-to-run-wmi-command-line-tools)
-   [處理 UAC 下的遠端連線](#handling-remote-connections-under-uac)
-   [UAC 對傳回給腳本或應用程式的 WMI 資料有何影響](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [相關主題](#related-topics)

## <a name="user-account-control"></a>使用者帳戶控制

在 UAC 下，本機 Administrators 群組中的帳戶有兩個 [*存取權杖*](/windows/desktop/SecGloss/a-gly)，一個具有標準使用者權限，另一個具有系統管理員許可權。 由於 UAC 存取權杖篩選，腳本通常會在標準使用者 token 下執行，除非它在更高的許可權模式下以系統管理員身分執行。 並非所有腳本都需要系統管理許可權。

腳本無法以程式設計方式判斷它們是以標準使用者安全性權杖還是系統管理員權杖來執行。 腳本可能會因為拒絕存取錯誤而失敗。 如果腳本需要系統管理員許可權，則必須在提高許可權的模式下執行。 WMI 命名空間的存取權會因腳本是否在提高許可權的模式中執行而有所不同。 某些 WMI 作業（例如取得資料或執行大部分的方法）不需要以系統管理員身分執行該帳戶。 如需預設存取權限的詳細資訊，請參閱 [存取 WMI 命名空間](access-to-wmi-namespaces.md) 和執行特殊許可權 [作業](executing-privileged-operations.md)。

由於使用者帳戶控制，執行腳本的帳戶必須在本機電腦的 Administrators 群組中，才能以較高的許可權執行。

您可以藉由執行下列其中一種方法，以較高的許可權執行腳本或應用程式：

**在提高許可權的模式中執行腳本**

1.  以滑鼠右鍵按一下 [開始] 功能表中的 [命令提示字元]，然後按一下 [以 **系統管理員身分執行**]，開啟 [命令提示字元] 視窗。
2.  使用工作排程器將腳本排程為提高許可權執行。 如需詳細資訊，請參閱 [執行工作的安全性](/windows/desktop/TaskSchd/security-contexts-for-running-tasks)內容。
3.  使用內建的系統管理員帳戶來執行腳本。

## <a name="account-needed-to-run-wmi-command-line-tools"></a>執行 WMI Command-Line 工具所需的帳戶

若要執行下列 [WMI Command-Line 工具](wmi-command-line-tools.md)，您的帳戶必須在 Administrators 群組中，而且必須從提升許可權的命令提示字元執行此工具。 內建的系統管理員帳戶也可以執行這些工具。

-   [**mofcomp.exe**](mofcomp.md)

-   [**wmic**](wmic.md)

    當您第一次在系統安裝之後執行 Wmic 時，必須從已提升許可權的命令提示字元執行。 除非 WMI 作業需要系統管理員許可權，否則，後續執行的 Wmic 可能不需要提高許可權模式。

-   [**winmgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

若要 (Wmimgmt.msc) 執行 [*Wmi 控制項*](gloss-w.md) ，並變更 wmi 命名空間安全性或審核設定，您的帳戶必須明確授與或在本機 Administrators 群組中的編輯安全性許可權。 內建的系統管理員帳戶也可以變更命名空間的安全性或審核。

Wbemtest.exe，Microsoft 客戶支援服務不支援的命令列工具，可以由不在本機 Administrators 群組中的帳戶執行，除非特定的作業需要通常授與系統管理員帳戶的許可權。

## <a name="handling-remote-connections-under-uac"></a>處理 UAC 下的遠端連線

無論您是連接到網域中或工作組中的遠端電腦，都會決定是否發生 UAC 篩選。

如果您的電腦是網域的一部分，請使用遠端電腦的本機 Administrators 群組中的網域帳戶來連接到目的電腦。 然後 UAC 存取權杖篩選不會影響本機 Administrators 群組中的網域帳戶。 請勿在遠端電腦上使用本機的非網域帳戶，即使帳戶是在 Administrators 群組中也一樣。

在工作組中，連接至遠端電腦的帳戶是該電腦上的本機使用者。 即使帳戶是在 Administrators 群組中，UAC 篩選也表示腳本會以標準使用者的身分執行。 最佳做法是在目的電腦上建立專用的本機使用者群組或使用者帳戶，特別是用於遠端連線。

因為帳戶從未具有系統管理許可權，所以必須調整安全性才能使用此帳戶。 授與本機使用者：

-   遠端啟動和啟動存取 DCOM 的許可權。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。
-   從遠端存取 WMI 命名空間 (遠端啟用) 的許可權。 如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。
-   存取特定安全物件的許可權，視物件所需的安全性而定。

如果您使用本機帳戶，可能是因為您是在工作組中，或是本機電腦帳戶，則可能會強制將特定工作提供給本機使用者。 例如，您可以授與使用者透過 SC.exe 命令、 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service)和 [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service)方法，或透過使用 gpedit.msc 的群組原則來停止或啟動特定服務的許可權。 某些安全物件可能不允許標準使用者執行工作，也不能提供改變預設安全性的方法。 在此情況下，您可能需要停用 UAC，讓本機使用者帳戶不會經過篩選，而是會成為完整的系統管理員。 請注意，基於安全性理由，停用 UAC 應該是最後的手段。

不建議藉由變更控制遠端 UAC 的登錄專案來停用遠端 UAC，但在工作組中可能是必要的。 登錄專案是 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **原則** \\ **系統** \\ **LocalAccountTokenFilterPolicy**。 當這個專案的值為零 (0) 時，會啟用遠端 UAC 存取權杖篩選。 當值為1時，會停用遠端 UAC。

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>UAC 對傳回給腳本或應用程式的 WMI 資料有何影響

如果腳本或應用程式是在 Administrators 群組中的帳戶下執行，但未以較高的許可權執行，則您可能無法取得傳回的所有資料，因為此帳戶是以標準使用者身分執行。 某些類別的 WMI [*提供者*](gloss-p.md) 不會將所有實例都傳回給標準使用者帳戶，或由於 UAC 篩選而未以完整系統管理員身分執行的系統管理員帳戶。

當 UAC 篩選帳戶時，下列類別不會傳回某些實例：

-   [**Win32 \_ 匯流排**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**Win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**Win32 \_ ComponentCategory**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**Win32 \_ LogicalProgramGroupItem**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**Win32 \_ LogicalProgramGroup**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**Win32 \_ NetworkConnection**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**Win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**Win32 \_ PrinterDriver**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**Win32 \_ PortResource**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**Win32 \_ DeviceMemoryAddress**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

當 UAC 篩選帳戶時，下列類別不會傳回某些屬性：

-   [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**Win32 \_ DCOMApplication**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**Win32 \_ 基礎板**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**Win32 \_ 未進行**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**Win32 \_ MotherboardDevice**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**Win32 \_ VideoController**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**Win32 \_ ParallelPort**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Win32 \_ >systemdriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**Win32 \_ IRQResource**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**Win32 \_ NetworkProtocol**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> <dt>

[存取 WMI 安全物件](access-to-wmi-securable-objects.md)
</dt> <dt>

[變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
