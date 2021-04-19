---
description: 您在設定應用程式的驗證等級時，便會決定當用戶端呼叫應用程式時，應執行何種程度的驗證。
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: 設定伺服器應用程式的驗證層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972969"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>設定伺服器應用程式的驗證層級

您在設定應用程式的驗證等級時，便會決定當用戶端呼叫應用程式時，應執行何種程度的驗證。 較高的驗證層級提供更高的安全性和資料完整性，不過通常會降低效能。 如需詳細資訊，請參閱 [用戶端驗證](client-authentication.md)。

**若要選取伺服器應用程式的驗證層級**

1.  以滑鼠右鍵按一下您要設定驗證的 COM + 應用程式，然後按一下 [ **屬性**]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  在 [ **呼叫的驗證等級** ] 方塊中，選取適當的層級。 層級如下所示，以最低到最高的安全性排序：

    -   **None**： 不會進行驗證。
    -   **連接**。 只有在進行連接之後才驗證認證。
    -   **呼叫**。 在一切呼叫的開始驗證認證。
    -   封 **包**。 驗證認證，並證實收到所有呼叫資料。 這是 COM+ 伺服器應用程式的預設值。
    -   封 **包完整性**。 驗證認證，並證實在傳輸中沒有呼叫資料被修改。
    -   封 **包隱私權**。 驗證認證，並加密封包，包括資料和寄件人的識別 (Identity) 和簽章。

4.  按一下 [確定]  。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



