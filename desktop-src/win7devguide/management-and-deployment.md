---
title: 管理和部署
description: 準備部署 Windows 7 的 IT 專業人員或開發人員將獲得更高的信心，並體驗較短的評估週期，因為映射功能和工具的改進。
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105b19ad01cb9208d05e77871be637fdadcb0532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933386"
---
# <a name="management-and-deployment"></a>管理和部署

準備部署 Windows 7 的 IT 專業人員或開發人員將獲得更高的信心，並體驗較短的評估週期，因為映射功能和工具的改進。 這些功能包括支援管理離線影像檔案中的應用程式、驅動程式和作業系統。 此外，映射的建立和管理作業也比較簡單，而且可供更廣泛的 IT 組織使用。 因為新的 IT 遷移工具和自動化的部署技術，所以將 Windows 7 部署到商務電腦也變得更容易且更快。

## <a name="windows-powershell-20"></a>Windows PowerShell 2.0

PowerShell 是一種完整的 Microsoft .NET managed 指令碼語言，同時具有互動式命令列介面和圖形化的腳本環境 (ISE) 。 它支援分支、迴圈、函數、調試、例外狀況處理和國際化。 PowerShell 2.0 是 Windows 7 的一部分，可針對 Windows 診斷、Microsoft Active Directory、Microsoft Internet Information Services (IIS) 等，提供許多增強功能和一組持續成長的 *Cmdlet* 。

PowerShell 2.0 遠端功能現在可讓使用者在一部或多部遠端電腦上，從執行 PowerShell 的單一電腦上執行命令。 開發人員也可以在 IIS 上裝載 PowerShell 來存取及管理其伺服器。

PowerShell 2.0 支援使用模組來分割和組織 PowerShell 腳本，這些模組可以散發和部署為獨立、可重複使用的單位。 它也包含 PowerShell 引擎和 Api 中的交易支援，這表示開發人員可以使用內建的交易 *Cmdlet* 來啟動、認可和回復交易。 此外，PowerShell 引擎包含事件支援來接聽、轉送和處理管理和系統事件。 您可以撰寫 PowerShell 應用程式來訂閱特定事件以進行同步或非同步處理。  (參閱 [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx)。 ) 

![windows powershell ise 螢幕擷取畫面](images/windows7-devguide-solidfig1-powershell.jpg)

圖 1. Windows PowerShell 是完整的 .NET managed 指令碼語言，同時具有互動式命令列 shell 和圖形 ISE

## <a name="windows-installer"></a>Windows Installer

Windows Installer 已更新，藉由減少建立安裝套件所需的自訂程式碼數量，並建立真正的每個使用者軟體安裝，來提高開發人員的效率。

多個封裝交易可讓開發人員使用 ' chainer '，以動態方式將封裝包含在交易中，以從多個封裝建立單一交易。 如果有一或多個套件未如預期般安裝，只要復原安裝即可。

內嵌 UI 處理常式使自訂 Ui 更容易整合，方法是在 Windows Installer 套件中內嵌自訂使用者介面處理常式。

內嵌的多套件 Chainer 可讓開發人員在多個套件之間啟用安裝事件。 例如，他們可以啟用隨選安裝事件、修復事件，以及在多個套件之間卸載事件。

新功能也可讓您建立真正的每一使用者安裝，包括支援每個使用者的程式檔案和「立即提升」功能，並透過部署映射服務與管理提供離線軟體清查和修補適用性檢查的支援。  (瞭解 [Windows Installer 5.0 中的新功能](../msi/what-s-new-in-windows-installer-5-0.md)。 ) 

 

 