---
description: WSAIoctl 函式可讓服務提供者提供提供者特有的功能延伸模組。
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific 擴充機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed627aefdfefda2bf4b395098f6680086fd37dd7a302d977d9bf238f77d89d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733568"
---
# <a name="provider-specific-extension-mechanism"></a>Provider-Specific 擴充機制

[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)函式可讓服務提供者提供提供者特有的功能延伸模組。 當然，這個機制假設應用程式知道特定的擴充功能，並同時瞭解所涉及的語法和語法。 服務提供者廠商通常會提供這類資訊。

若要叫用擴充功能，應用程式必須先要求所需函式的指標。 這是透過 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式使用 SIO 取得延伸模組函式 \_ \_ \_ \_ 指標命令程式碼來完成。 要 **WSAIoctl** 的輸入緩衝區包含所需擴充功能函式的識別碼，而輸出緩衝區包含函式指標本身。 然後，應用程式就可以直接叫用擴充功能，而不需透過 Ws2 \_32.dll。

指派給延伸模組函式的識別碼是由服務提供者廠商所配置 (Guid) 的全域唯一識別碼。 建立延伸模組函式的廠商呼籲，以發佈函式的完整詳細資料，包括函數原型的語法。 這可讓多個服務提供者廠商提供常見且熱門的擴充功能。 應用程式可以取得函式指標並使用函式，而不需要知道任何有關執行函數的特定服務提供者。

在 Windows Vista 和更新版本上，系統會直接從 winsock DLL 匯出新的 Winsock 系統延伸模組，因此不需要 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)函式就能載入這些擴充功能。 Windows Vista 和更新版本上提供的新擴充功能，包括從 *Ws2 \_32.dll* 匯出的 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)和 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)函數。

 

 
