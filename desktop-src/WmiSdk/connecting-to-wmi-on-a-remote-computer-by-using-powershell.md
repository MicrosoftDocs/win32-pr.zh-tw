---
description: 使用 PowerShell 從遠端連線至 WMI
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: 使用 PowerShell 從遠端連線至 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d499c59ee6774b1e972e192dfc2c0d1228469196c66e8f3feb80d1c9d6339c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679868"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>使用 PowerShell 從遠端連線至 WMI

Windows PowerShell 提供簡單的機制，以連接到遠端電腦上 Windows Management Instrumentation (WMI) 。 WMI 中的遠端連線會受到[Windows 防火牆](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))、DCOM 設定，以及[ (UAC) 的使用者帳戶控制](/previous-versions/aa905108(v=msdn.10))所影響。 如需有關設定遠端連線的詳細資訊，請參閱[從 Windows Vista 開始遠端連線至 WMI](connecting-to-wmi-remotely-starting-with-vista.md)。

本主題中的範例是 [以 Vbscript 連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)為基礎。 本主題中的所有範例都會使用 [>get-wmiobject 指令程式](/previous-versions//dd315295(v=technet.10)) 。 如需詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd315295(v=technet.10))。

## <a name="windows-powershell-examples"></a>Windows PowerShell 範例

建立遠端電腦的連線時，使用者可以指定連線資訊，例如遠端電腦名稱稱、認證，以及連線的驗證層級。 下列範例說明如何使用不同的認證組來連接到遠端電腦，以及如何存取 WMI 資訊。

下列 Windows PowerShell 範例會示範如何設定模擬等級：


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



在上述範例中，使用者會使用與登入 (網域和使用者名稱) 相同的認證，連接到遠端電腦。 使用者也要求使用模擬。 與原始 VBScript 範例不同的是，不需要使用「標記」字串，因為模擬層級是由「模擬」屬性所設定。 根據預設，模擬層級設定為 3 (模擬) 。

此範例會列出在遠端電腦上執行的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 類別的所有實例。

> [!Note]  
> 您應該指定要在遠端電腦上連接的 WMI 命名空間，因為不同電腦上的預設命名空間可能不相同。

 

下列 Windows PowerShell 範例示範如何使用不同的認證連接到遠端電腦，以及如何將模擬等級設定為3，也就是模擬：


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



在上述範例中，電腦名稱稱已指派給 $Computer 變數。 使用者會使用特定的認證來連線到遠端電腦 (網域和使用者名稱) ，並要求驗證層級的模擬。

> [!Note]  
> 使用「音符號」（ (\`) ）來表示分行符號。 它相當於 VBScript 中 () 的底線字元 \_ 。

 

下列 Windows PowerShell 範例會在每一部電腦上建立遠端電腦名稱稱陣列，然後顯示隨插即用裝置（ [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)的實例）的名稱，以連接到同一網域中的一組遠端電腦：


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> 若要執行上述 Windows PowerShell 腳本，您必須是遠端電腦上的系統管理員。 此外，與上述範例相關，請注意下列事項：

 

-   陣列中的電腦名稱稱必須以引號括住，因為它們是字串。
-   [>Get-wmiobject](/previous-versions//dd315295(v=technet.10))所傳回的物件會指派給 $ColItems 變數。
-   範圍運算子會 \[ \] 將隨插即用裝置的清單限制為48個實例。 如需詳細資訊，請參閱 [關於 \_ 運算子](/previous-versions//dd347588(v=technet.10))。
-   " \| " 是管線字元。 ColItems 傳回的物件會傳送至 [格式清單]( /previous-versions//dd347700(v=technet.10)) Cmdlet。

下列 Windows PowerShell 範例可讓您連接到不同網域上的遠端電腦。 此範例也會顯示遠端電腦上 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 實例的處理常式名稱。


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> 若要執行上述 Windows PowerShell 腳本，您必須是遠端電腦上的系統管理員。

 

在上述範例中，使用者會連接到不同網域的遠端電腦，並指定慣用的地區設定。 [取得認證](/previous-versions//dd315327(v=technet.10))命令會要求使用者的認證，並將認證指派給物件。 此範例也會列出電腦上執行的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 類別的實例名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
