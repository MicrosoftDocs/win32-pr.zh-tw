---
description: 您可以使用 Win32 \_ 進程建立，在遠端電腦上執行腳本或應用程式。 不過，基於安全性理由，此程式不能是互動式的。 在 \_ 本機電腦上呼叫 Win32 進程時，進程可以是互動式的。
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: 使用 WMI 從遠端建立進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694472"
---
# <a name="creating-processes-remotely-using-wmi"></a>使用 WMI 從遠端建立進程

您可以使用 [**Win32 \_ 進程建立**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) ，在遠端電腦上執行腳本或應用程式。 不過，基於安全性理由，此程式不能是互動式的。 在本機電腦上呼叫 **Win32 \_ 進程** 時，進程可以是互動式的。

> [!WARNING]
> 本主題說明使用 WMI 建立遠端進程的一般程式。 如果您只是想要在遠端系統上執行腳本，請參閱 [從 Windows Vista 開始遠端連線到 wmi](connecting-to-wmi-remotely-starting-with-vista.md)，或 [使用 Windows PowerShell 連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)。 如需有關使用 PowerShell 進行遠端處理的一般資訊，請參閱執行 [遠端命令](https://technet.microsoft.com/library/dd819505.aspx)。

 

遠端進程沒有使用者介面，但會列在 **工作管理員** 中。 如果帳戶具有根 cimv2 命名空間的 **Execute 方法** 許可權，在本機建立的進程可以在任何帳戶下執行 \\ 。 如果帳戶具有 [ **執行方法** ] 和 [ **遠端啟用** 根 cimv2 的許可權]，則遠端建立的進程可以在任何帳戶下執行 \\ 。 [ **執行方法** ] 和 [ **遠端啟用** ] 許可權是在主控台的 WMI 控制中設定。 如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。

您可以使用 [**Win32 \_ register-scheduledjob**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) 建立遠端的互動式進程。 但是由 **Win32 \_ register-scheduledjob** 啟動的進程會在 LocalSystem 帳戶下執行，而該帳戶可授與過多的許可權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)
</dt> <dt>

[連接到第三台電腦-委派](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
