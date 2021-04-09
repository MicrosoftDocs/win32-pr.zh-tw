---
title: BITS PowerShell 命令的受管理參考
description: 背景智慧型傳送服務 (位) 4.0 可以使用 Windows PowerShell Cmdlet 來管理傳送作業。
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bd195d2202849c2bf2df580d159ee401911c51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842523"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>BITS PowerShell 命令的受管理參考

背景智慧型傳送服務 (位) 4.0 可以使用 Windows PowerShell Cmdlet 來建立和管理檔案下載和上傳傳送作業。

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

適用于 BITS 的 Windows PowerShell Cmdlet 提供許多與 bitsadmin 命令列公用程式相同的功能。 不過，Windows PowerShell 也會執行下列動作：

-   使用可延伸和管理導向的指令碼語言來自動化 BITS 工作。
-   提供適用于所有作業相關工作的單一工具。

> [!Note]  
> 若要使用這些命令，您必須先使用命令匯入 BITS PowerShell 模組 `Import-Module BitsTransfer` 。 如需詳細資訊，請參閱下列 [TechNet 文章](/previous-versions/technet-magazine/ff382721(v=msdn.10))。

 

如需有關使用 Windows Powershell 的詳細資訊，請參閱 [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx)。

## <a name="bits-powershell-classes"></a>BITS PowerShell 類別

**命名空間**： Microsoft. BackgroundIntelligentTransfer. 管理

**元件**： System. Management. Automation

這些位命令類別是由 Windows PowerShell 所執行。 這些類別包含在此軟體發展工具組中， (SDK) 僅供完整性之用。 這些類別的成員不能直接使用，也不能用來衍生其他類別。



| 類別                           | 描述                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AddBitsFileCommand**          | 將一或多個檔案新增至現有的 BITS 傳送工作。<br/> 如需有關參數的詳細資訊和範例，請參閱 [add-bitsfile](/previous-versions//dd347701(v=technet.10)) Cmdlet。<br/>                       |
| **ClearBitsTransferCommand**    | 取消 BITS 傳送工作。<br/> 如需參數的詳細資訊和範例，請參閱 [BitsTransfer]( /previous-versions//dd347701(v=technet.10)) Cmdlet。<br/>                                          |
| **CompleteBitsTransferCommand** | 完成 BITS 傳送工作。<br/> 如需參數的詳細資訊和範例，請參閱 [BitsTransfer]( /previous-versions//dd347701(v=technet.10)) Cmdlet。<br/>                                     |
| **GetBitsTransferCommand**      | 抓取現有 BITS 傳送工作的相關聯 BitsJob 物件。<br/> 如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。<br/> |
| **NewBitsTransferCommand**      | 建立新的 BITS 傳送工作。<br/> 如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。<br/>                                           |
| **ResumeBitsTransferCommand**   | 繼續 BITS 傳送工作。<br/> 如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。<br/>                                            |
| **SetBitsTransferCommand**      | 修改現有 BITS 傳送工作的屬性。<br/> 如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。<br/>                  |
| **SuspendBitsTransferCommand**  | 暫停 BITS 傳送工作。<br/> 如需有關參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。<br/>                                          |



 

 

