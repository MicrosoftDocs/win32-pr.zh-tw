---
description: 說明如何執行密碼篩選匯出功能的考慮。
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: 密碼篩選程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998449"
---
# <a name="password-filter-programming-considerations"></a>密碼篩選程式設計考慮

在執行 [*密碼篩選*](/windows/desktop/SecGloss/p-gly) 匯出函式時，請記住下列考慮：

-   使用 [*明文*](/windows/desktop/SecGloss/p-gly) 密碼時，請格外小心。 透過網路傳送純文字密碼可能會危及安全性。 網路「嗅探程式」可以輕易地監看純文字密碼流量。
-   在釋放記憶體之前呼叫 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函式，以清除用來儲存密碼的所有記憶體。
-   傳入密碼通知和篩選常式的所有緩衝區都應視為唯讀。 將資料寫入這些緩衝區可能會造成不穩定的行為。
-   所有密碼通知和篩選常式都應該是安全線程。 使用重要區段或其他同步程式設計技術，在適當的情況下保護資料。
-   密碼通知和篩選只會在裝載帳戶的電腦上進行。
-   所有網域控制站都是可寫入的，因此密碼篩選器套件必須存在於所有網域控制站上。

    **Windows NT 4.0 網域：** 網域帳戶的通知只會在網域主控站上進行。 除了主域控制站以外，密碼篩選器套件應該安裝在所有備份網域控制站上，以允許在伺服器角色變更時繼續進行通知。

-   所有密碼篩選 Dll 都是在本機系統帳戶的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 中執行。



| 如需下列資訊                                                                                                                     | 請參閱                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| 如何安裝及註冊您自己的 [*密碼篩選*](/windows/desktop/SecGloss/p-gly) DLL。 | [安裝和註冊密碼篩選 DLL](installing-and-registering-a-password-filter-dll.md) |
| Microsoft 提供的密碼篩選 DLL。                                                                                            | [強式密碼強制執行和 Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| 匯出由密碼篩選 DLL 所執行的函式。                                                                                    | [密碼篩選函數](management-functions.md)                          |



 

 

 
