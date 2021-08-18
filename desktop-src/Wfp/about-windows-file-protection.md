---
description: Windows資源保護 (WRP) 防止取代安裝為作業系統一部分的基本系統檔案、資料夾和登錄機碼。
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: 關於 Windows 資源保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d06110c668e48a401cc329d79982e7c1b2746408ce45da9b7b3dffaca40b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134193"
---
# <a name="about-windows-resource-protection"></a>關於 Windows 資源保護

Windows資源保護 (WRP) 防止取代安裝為作業系統一部分的基本系統檔案、資料夾和登錄機碼。 從 Windows Server 2008 和 Windows Vista 開始提供。 修改受 WRP 保護之資源的完整存取權，僅限 TrustedInstaller。 WRP 保護的資源只能使用[支援的資源取代機制](supported-file-replacement-mechanisms.md)搭配 Windows 模組安裝程式服務來變更。 保護這些資源可防止應用程式和作業系統失敗。

應用程式不應該嘗試修改受 WRP 保護的資源，因為這些資源是由 Windows 和其他應用程式所使用。 如果應用程式嘗試修改受 WRP 保護的資源，則可能會有下列結果。

-   嘗試取代、修改或刪除重要 Windows 檔案或登錄機碼的應用程式安裝程式可能無法安裝應用程式，並且會收到錯誤訊息，指出已拒絕存取資源。
-   嘗試新增或移除子機碼或變更受保護登錄機碼值的應用程式可能會失敗，並會收到錯誤訊息，指出已拒絕存取資源。
-   依賴將任何資訊寫入受保護登錄機碼、資料夾或檔案的應用程式可能會失敗。

WRP 是 Windows 檔案保護 (WFP) 的新名稱。 WRP 可保護登錄機碼和資料夾，以及基本的系統檔案。 在 Microsoft Windows Server 2003 和 Windows XP 中都有提供 WFP。 WRP 會取代 Windows Server 2008 和 Windows Vista 中的 WFP。

下列主題將說明 WRP：

-   [受保護的資源清單](protected-file-list.md)
-   [偵測資源取代](detecting-file-replacement.md)
-   [支援的資源取代機制](supported-file-replacement-mechanisms.md)
-   [系統檔案檢查程式](system-file-checker.md)
-   [遠端系統管理考慮](remote-administration-considerations.md)

 

 



