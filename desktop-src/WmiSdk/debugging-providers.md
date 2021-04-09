---
description: 提供者（除非它們是在應用程式內執行的低耦合提供者）會載入 Wmiprvse.exe 進程，而不會透過 Winmgmt.exe 程式 Svchost.exe。 如需詳細資訊，請參閱提供者裝載和安全性。
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: 偵錯工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943874"
---
# <a name="debugging-providers"></a>偵錯工具

提供者（除非它們是在應用程式內執行的低 [*耦合提供者*](gloss-d.md) ）會載入 Wmiprvse.exe 進程，而不會透過 Winmgmt.exe 程式 Svchost.exe。 如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

在中斷點停止時，Visual Studio 偵錯工具會凍結整個提供者主機進程，這通常是共用主控制項 Wmiprvse.exe。 這可防止在該進程中裝載的任何其他元件（包括 WMI 伺服器總管擴充功能）進行操作。 同時也會封鎖呼叫提供者的用戶端應用程式。 由於提供者載入至 WMI 服務進程 (Winmgmt.exe) ，因此 Windows 2000 和更早版本中的問題會更糟。

如果您在另一個實例中執行 WMI 伺服器總管則 Visual Studio IDE 不會凍結，而且您可以釋放中斷點。 建議您在開發階段期間，于不同的裝載進程中執行您的提供者，以便在中斷點停止時，只會凍結主控提供者的進程。 Wmi 中的其他函式仍可繼續存取 wmi 伺服器總管以及任何其他 WMI 應用程式或腳本。 此外，如果您的提供者損毀，就不會影響載入至相同主機進程的其他提供者作業。

若要讓提供者在自己的主機進程中載入，請修改提供者註冊，將 [**\_ \_ Win32Provider. HostingModel**](--win32provider.md)屬性設定為， `NetworkServiceHost:[MyProvider]` 其中 MyProvider 可以是可唯一識別提供者的任何字串。 例如，使用 Win32Provider 的 **\_ \_ ClsId** 值。 當您的提供者已準備好寄送時，請將 **\_ \_ Win32Provider HostingModel** 回預期的值，例如 **NetworkServiceHost**。

如果您不是要對提供者載入進行偵錯工具，您可以呼叫 [**MSFT \_ 提供者類別的 load 方法**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) 來強制載入您的提供者，然後附加至已載入 DLL 的 Wmiprvse.exe 進程，然後視需要進行偵錯工具。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[WMI 疑難排解類別](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
