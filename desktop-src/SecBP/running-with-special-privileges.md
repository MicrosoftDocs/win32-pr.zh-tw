---
description: 某些函數需要特殊許可權才能正確執行。
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: 以特殊許可權執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9bcd9db0f54c14c5a66d452e394252e6dacad933a92157f59811af90f84a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127268"
---
# <a name="running-with-special-privileges"></a>以特殊許可權執行

某些函數需要特殊 [許可權](/windows/desktop/SecAuthZ/privileges) 才能正確執行。 在某些情況下，函數只能由特定使用者或特定群組的成員執行。 最常見的需求是使用者是本機系統管理員。 其他函式要求使用者的帳戶必須啟用特定許可權。

為了降低未經授權的程式碼能夠取得控制權的可能性，系統應該以所需的最低許可權來執行。 需要呼叫需要特殊許可權之函式的應用程式，可能會讓系統保持在駭客攻擊的狀態。 這類應用程式應該設計成在短時間內執行，而且應該告知使用者相關的安全性含意。

如需如何以不同的使用者執行，以及如何在您的應用程式中啟用許可權的詳細資訊，請參閱下列主題：<dl>

[以系統管理員許可權執行](running-with-administrator-privileges.md)  
[要求使用者提供認證](asking-the-user-for-credentials.md)  
[變更權杖中的許可權](changing-privileges-in-a-token.md)  
[將許可權指派給帳戶](assigning-privileges-to-an-account.md)  
</dl>

 

 
