---
description: 使用 WMI 取得用戶端腳本和應用程式資料，或從應用程式提供資料給 WMI 的藍圖。
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: 使用 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d1556d321441c7e6a3191bf95e85db356e7ba9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475314"
---
# <a name="using-wmi"></a>使用 WMI

您可以從用戶端應用程式和腳本使用 WMI。 它提供的基礎結構可讓您輕鬆地探索和執行管理工作。 此外，您可以藉由建立自己的 WMI 提供者，新增至一組可能的管理工作。

> [!Note]  
> 下一代的 WMI 可用來撰寫應用程式和腳本，可透過 Windows 管理基礎結構 (MI) 取得。 如需詳細資訊，請參閱 [MI 提供者和用戶端](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page)。

 

本節將討論下列主題：

-   [從 WMI 取得資料](#obtaining-data-from-wmi)
-   [將資料提供給 WMI](#providing-data-to-wmi)
-   [WMI 的重要工作](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>從 WMI 取得資料

下列程式描述如何藉由撰寫腳本或應用程式，從 WMI 取得資料。

**藉由撰寫腳本或應用程式從 WMI 取得資料**

1.  決定要使用的語言。 如需腳本的詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。 如需 c + + 的詳細資訊，請參閱 [使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)。 如需使用 c # 或 WMI .NET 的詳細資訊，請參閱 [WMI .Net 總覽](/previous-versions/)。

    您可以用多種語言來查看或操作 WMI 資料。 下表列出的主題描述如何使用腳本和應用程式語言來取得資料。

    

    
| 應用程式語言 | 主題 | 
|----------------------|-------|
| 以 Microsoft ActiveX 腳本裝載撰寫的腳本，包括 Visual Basic 腳本版本 (VBScript) 和 Perl<br /> | <a href="scripting-api-for-wmi.md">適用于 WMI 的腳本 API</a>。<br /> 從 <a href="creating-a-wmi-script.md">建立 WMI 腳本</a>開始。<br /> 如需腳本範例，請參閱 <a href="wmi-tasks-for-scripts-and-applications.md">腳本和應用程式的 WMI</a> 工作和 TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> 腳本存放庫。<br /> | 
| Windows PowerShell<br /> | <a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">使用 Windows PowerShell 開始使用</a><br /> WMI PowerShell Cmdlet，例如 <a href="/previous-versions//dd315295(v=technet.10)">>get-wmiobject</a>。<br /> | 
| Visual Basic 應用程式<br /> | <a href="scripting-api-for-wmi.md">適用于 WMI 的腳本 API</a>。<br /> | 
| Active Server Page<br /> | <a href="scripting-api-for-wmi.md">適用于 WMI 的腳本 API</a>。<br /> 從 <a href="creating-active-server-pages-for-wmi.md">建立 WMI 的 Active Server 頁面</a>開始。<br /> | 
| C++ 應用程式<br /> | <a href="com-api-for-wmi.md">適用于 WMI 的 COM API</a>。<br /> 首先，使用 c + + 和<a href="wmi-c---application-examples.md">Wmi c + + 應用程式範例</a><a href="creating-a-wmi-application-using-c-.md">來建立 wmi 應用程式</a> (包含) 的範例。<br /> | 
| .NET Framework 以 c #、Visual Basic .net 或 J 撰寫的應用程式#<br /> | 在「 <a href="/previous-versions//hh872326(v=vs.85)"><strong>管理基礎結構</strong></a> 」命名空間中的類別。<br /><blockquote>    [!Note]<br /><strong>System. Management</strong> 是涵蓋 WMI managed 程式碼的原始命名空間。 但是， <strong>管理系統</strong> 的基礎技術通常會比更慢，而且也不會調整及 <a href="/previous-versions//hh872326(v=vs.85)"><strong>管理基礎結構</strong></a>。 因此，不建議您針對新的專案使用 [ <strong>系統管理</strong> ]。  (如需有關 <strong>系統管理</strong>的詳細資訊，請參閱 <a href="/previous-versions/bb404655(v=vs.90)">WMI .net 總覽</a>。 )     </blockquote><br /> | 


    

     

2.  確定您與遠端電腦的連線可以運作。

    如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

3.  連接至遠端電腦上的 WMI 需要正確的安全性設定，如 [維護 WMI 安全性](maintaining-wmi-security.md)中所述。 下表列出的主題描述如何使用腳本和應用程式語言來設定安全性設定。

    

    | 語言                                                      | 主題                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 任何語言的腳本，Visual Basic 應用程式<br/> | [使用 VBScript 設定預設進程安全性等級](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | Active Server Page<br/>                                | [針對 WMI ASP 腳本設定 IIS 5 和更新版本](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [使用 c + + 設定預設進程安全性等級](setting-the-default-process-security-level-using-c-.md) ，並 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  連接到 WMI 之後，您可以透過查詢和列舉來取得資料。

    如需詳細資訊，請參閱[使用 WQL](querying-with-wql.md)[操作類別和實例資訊](manipulating-class-and-instance-information.md)和查詢。

5.  登錄資料可透過 WMI 取得，而您可以建立新的索引鍵和值，或是修改現有的金鑰和值。

    如需詳細資訊，請參閱 [修改系統登錄](modifying-the-system-registry.md)。

6.  您可以透過 WMI （在系統重新開機或永久）之間暫時訂閱事件通知。

    如需詳細資訊，請參閱 [監視事件](monitoring-events.md) 和 [接收 WMI 事件](receiving-a-wmi-event.md)。

7.  您可以透過 WMI 取得系統的效能計數器資料。

    系統效能程式庫計數器會轉換成 WMI 類別。 如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)。

8.  [腳本和應用程式的 wmi](wmi-tasks-for-scripts-and-applications.md) 工作說明如何使用 wmi 進行許多系統管理工作。

## <a name="providing-data-to-wmi"></a>將資料提供給 WMI

下列程式描述如何藉由撰寫提供者，將資料提供給 WMI。

**撰寫提供者以將資料提供給 WMI**

-   決定要寫入的提供者類型。

    您無法在 VBScript 中寫入 WMI 提供者。 不過，您可以採取數種其他方法來撰寫 WMI COM 提供者：

    -   使用 Visual Studio 中的 WMI ATL Wizard。

        這種方法會建立非受控 COM 提供者。 如需詳細資訊，請參閱 [新增 Wmi 執行個體提供者](./writing-an-instance-provider.md) 和 [新增 Wmi 事件提供者](./writing-an-event-provider.md)。

    -   直接在任何整合式開發環境中使用 COM。

        這種方法會建立非受控 COM 提供者。

    -   使用 .NET Framework 中的 WMI 來建立 managed 程式碼提供者。

        這種方法會建立 managed 程式碼提供者。 Managed 程式碼提供者可以用任何 .NET Framework 語言撰寫，比 wmi COM 提供者更容易撰寫，並可從 wmi [*CIM*](gloss-c.md)型類別（例如 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider)）取得資料。 不過，.NET Framework WMI 提供者有一些限制。 如需詳細資訊，請參閱 [使用 WMI 管理應用程式](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))。

    -   不建議使用 [提供者架構類別](wmi-c-classes.md) 。

        提供者架構已被 WMI ATL 嚮導取代，直接使用 COM 或 .NET Framework 提供者。 不再建議使用提供者架構類別建立 WMI COM 提供者。 下表列出說明如何使用 COM 或 .NET Framework 提供者的主題。

    

    | 提供者                                                      | 主題                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | 與 WMI 相同的進程中的 COM 提供者<br/>            | [將資料提供給 WMI](providing-data-to-wmi.md)<br/>                                           |
    | COM 低耦合提供者<br/>                             | [將提供者併入應用程式中](incorporating-a-provider-in-an-application.md)<br/> |
    | c # 或 Visual Basic .net 中的 .NET Framework 提供者<br/> | [使用 WMI 管理應用程式](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>WMI 的重要工作

下列主題提供有關使用 WMI 來監視和控制企業元件的資訊。



| 主題                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [腳本和應用程式的 WMI 工作](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | 描述如何在執行一般電腦和網路管理工作的腳本和應用程式中，尋找要使用的正確 WMI 類別和程式，例如為遠端電腦新增新的印表機連線，或尋找電腦上所有已安裝的修補程式。<br/>                                                                            |
| [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)<br/>                                                     | 適用于 ActiveX 物件的任何指令碼語言（如 VBScript 或 Perl）都可以存取 WMI 資料。 應用程式可以在 c + + 中使用[適用于 wmi 的 COM API](com-api-for-wmi.md)或 Visual Basic 中的 wmi，使用 >wbemdisp.tlb .tlb[類型程式庫](using-the-wmi-scripting-type-library.md)和[適用于 wmi 的腳本 API](scripting-api-for-wmi.md)來存取 wmi。<br/> |
| [連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | 描述腳本、應用程式和提供者如何在遠端電腦上建立與 WMI 的連接，以取得資料或控制硬體和軟體。<br/>                                                                                                                                                                                                   |
| [使用 Windows PowerShell 連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | 說明如何使用 Windows PowerShell 在遠端電腦上建立與 WMI 的連接，以取得資料或控制硬體和軟體。<br/>                                                                                                                                                                                                            |
| [監視事件](monitoring-events.md)<br/>                                                                                           | 說明如何藉由建立暫時或永久的 WMI 事件取用者來取得事件通知。<br/>                                                                                                                                                                                                                                                           |
| [將資料提供給 WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI 會將動態管理資料提供給用戶端腳本和應用程式，方法是從提供者取得它。<br/>                                                                                                                                                                                                                                                    |
| [在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | 描述如何在64位系統上存取提供者寫入器的非預設提供者和考慮。<br/>                                                                                                                                                                                                                                                    |



