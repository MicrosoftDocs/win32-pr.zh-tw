---
title: Active Directory 擴充功能的偵錯工具
description: 本主題中記載的 Microsoft Active Directory Directory 服務屬性工作表、內容功能表和物件建立嚮導延伸模組會實作為 COM 的內部進程伺服器。
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8d9646f4ccc2e8c740a81ddb48422881744f5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023262"
---
# <a name="debugging-an-active-directory-extension"></a>Active Directory 擴充功能的偵錯工具

本主題中記載的 Microsoft Active Directory Directory 服務屬性工作表、內容功能表和物件建立嚮導延伸模組會實作為 COM 的內部進程伺服器。 也就是說，每個延伸模組都是在主機進程內容中執行的 DLL。 若要對延伸模組進行偵錯工具，必須將擴充功能與應用程式建立關聯，並在偵錯工具中執行應用程式。

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a>在 Windows Shell 中顯示 Active Directory 擴充功能的偵錯工具

在 Explorer.exe 進程的內容中，會載入 Windows shell 中顯示的 Active Directory 延伸模組。 這些擴充功能可以像標準 shell 擴充功能一樣地進行調試。 如需有關偵錯工具擴充功能的詳細資訊，請參閱 [使用 shell 進行的調試](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85))程式。

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a>Active Directory MMC 中所顯示 Active Directory 擴充功能的調試 Snap-Ins

Active Directory 系統管理 MMC 嵌入式管理單元中顯示的 Active Directory 延伸模組會載入 Microsoft Management Console 的內容中。 若要 debug 擴充功能，請在本機系統上找出 Mmc.exe，並將偵錯工具設定為使用此應用程式來進行偵錯工具。 在大部分的系統上，Mmc.exe 位於 Windows 系統目錄中，例如 C： \\ WINNT \\ System32。 視偵錯工具而定，您可能也不需要將擴充 DLL 設定為也要由偵錯工具載入。 許多偵錯工具也可讓您將偵錯工具附加至執行中的 MMC 進程。 如需詳細資訊，請參閱您的偵錯工具使用者指南。

讓 MMC 自動載入特定的嵌入式管理單元是很方便的。 若要這樣做，請將應用程式引數設定為 SERVICES.MSC 檔案的路徑和檔案名。 這可以是系統安裝的 SERVICES.MSC 檔案，也可以是您建立的檔案。 您可以依照下列步驟來建立 SERVICES.MSC 檔案。

1.  執行 Mmc.exe。
2.  **選取**  -  mmc 功能表中的 [檔案 **新增/移除嵌入式管理單元 ...** ]，然後選取所需的嵌入式管理單元，以載入所需的嵌入式管理單元。
3.  選取 MMC 功能表中的 [   -  **另存** 新檔]，以儲存 services.msc 檔案。

如果您未設定啟動 SERVICES.MSC 檔案，當您在偵錯工具中執行應用程式時，必須手動載入所需的嵌入式管理單元。

當主應用程式在偵錯工具中執行時，偵錯工具可能會顯示一則警告訊息，指出正在執行的應用程式不包含任何 debug 符號。 這是預期的情況，而且可以安全地忽略，因為您實際上是在偵錯工具，而不是主應用程式。

在大部分的情況下，將不會呼叫擴充功能，直到使用者執行某些動作，而導致載入和初始化擴充功能為止。 例如，如果您要對使用者物件所顯示的內容功能表延伸進行偵錯工具，則在第一次顯示使用者物件的內容功能表之前，將不會載入擴充功能。

您現在應該能夠設定中斷點並查看調試輸出。 如果延伸模組似乎未載入，請在擴充功能的 [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式中設定中斷點。 如果未呼叫 **DllGetClassObject** ，可能是因為擴充功能未正確註冊。

當偵錯工具完成時，結束 MMC 和偵錯工具應該會正常地卸載。

 

 