---
description: 通訊端控制碼可以選擇性地成為 Windows 通訊端2中的檔案控制代碼。 來自 Winsock 提供者的通訊端控制碼可搭配其他非 Winsock 函數使用，例如 ReadFile、WriteFile、ReadFileEx 和 WriteFileEx。
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: 通訊端控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6ca8ed935819e018a59c52fb43dcf816530c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978899"
---
# <a name="socket-handles"></a>通訊端控制碼

通訊端控制碼可以選擇性地成為 Windows 通訊端2中的檔案控制代碼。 來自 Winsock 提供者的通訊端控制碼可搭配其他非 Winsock 函數使用，例如 [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)、 [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex)。

**XP1 \_ ifs \_ 處理** 提供者的通訊協定資訊結構中的成員，會決定提供者的通訊端控制碼是否為可安裝的檔案系統 (IFS) 控制碼。 您可以使用 [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) 和 [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)以外的其他非 (Winsock 函式，來使用可使用 IFS 控制碼的通訊端控制碼，而不會受到任何效能影響，例如) 。 搭配非 Winsock 函式使用時，任何非 IFS 通訊端控制碼 (**ReadFile** 和 **WriteFile**，例如) 導致提供者與檔案系統之間的互動，其中牽涉到額外的處理負荷，因此可能會造成顯著的效能影響。 搭配非 Winsock 函式使用通訊端控制碼時，從基底檔案系統傳播的錯誤碼不一定會對應到 Winsock 錯誤碼。 因此，建議您只搭配 Winsock 函數使用通訊端控制碼。

通訊端控制碼不應搭配 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函式使用。 有多層式服務提供者 (Lsp) 可能會導致這種情況失敗，而且目的地進程無法匯入通訊端控制碼。

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

Windows 通訊端2已展開特定功能，以使用控制碼在通訊端之間傳輸資料。 這些函式提供通訊端特定的優點，以傳輸資料並包含 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)和 [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa)。

 

 
