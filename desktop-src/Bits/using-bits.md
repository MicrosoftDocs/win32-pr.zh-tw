---
title: 使用 BITS
description: 使用 BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- 背景智慧型傳送服務
- 背景智慧型傳送服務，工作
- 檔案傳輸位
- 使用位位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965254"
---
# <a name="using-bits"></a>使用 BITS

下列步驟示範如何使用背景智慧型傳送服務 (位)  [介面](bits-interfaces.md)來執行檔案傳輸。

**執行檔案傳輸**

1.  [連接到 BITS 服務](connecting-to-the-bits-service.md)
2.  [建立傳送作業](creating-a-job.md)
3.  [將檔案新增至作業](adding-files-to-a-job.md)
4.  [啟動工作](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [判斷 BITS 是否已成功傳輸檔案](determining-the-status-of-a-job.md)
6.  [完成工作](completing-and-canceling-a-job.md)

先前的步驟示範如何使用作業的預設屬性值來傳送檔案。 您可以藉由變更一或多個作業的屬性值來變更預設行為。 例如，您可以變更作業相對於佇列中其他作業的處理優先權、指定您自己的 proxy 設定，以及註冊在 BITS 傳輸檔案時接收事件通知。 如需詳細資訊，請參閱 [設定和取出作業的屬性](setting-and-retrieving-the-properties-of-a-job.md)。

Windows PowerShell 提供簡單的機制來管理許多 BITS 工作。 本節包含下列主題，說明如何搭配使用 Windows PowerShell Cmdlet 與位：

-   [使用 Windows PowerShell 建立 BITS 傳送工作](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [使用 WinRM Windows PowerShell Cmdlet 來管理 BITS 傳送工作](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [使用 WMI Windows PowerShell Cmdlet 來管理 BITS Compact Server](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> 從1607版 Windows 10 開始，您也可以執行 PowerShell Cmdlet，並使用 BITSAdmin 或其他應用程式，從連線到另一部電腦的 PowerShell 遠端命令列（ (實體或虛擬) ）使用 BITS [介面](bits-interfaces.md) 。 使用 PowerShell Direct 命令列將 [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) 命令列使用於相同實體電腦上的虛擬機器時，無法使用此功能。使用 WinRM Cmdlet 時，無法使用此功能。
>
> 從遠端 PowerShell 會話建立的 BITS 作業將會在該會話的使用者帳戶內容下執行，而且只有在至少有一個作用中的本機登入會話或與該使用者帳戶相關聯的遠端 PowerShell 會話時，才會進行進度。 如需詳細資訊，請參閱 [管理 PowerShell 遠端會話](using-windows-powershell-to-create-bits-transfer-jobs.md)。

 

本節也包含下列主題：

-   [使用 BITS 的最佳作法](best-practices-when-using-bits.md)
-   [列舉傳送佇列中的作業](enumerating-jobs-in-the-transfer-queue.md)
-   [列舉作業中的檔案](enumerating-files-in-a-job.md)
-   [處理錯誤](handling-errors.md)
-   [從上傳-回復作業取出回復](retrieving-the-reply-from-an-upload-reply-job.md)

如需使用 BITS 介面的範例程式碼，請參閱 [Bits 範例和工具](bits-samples-and-tools.md)。

 

 