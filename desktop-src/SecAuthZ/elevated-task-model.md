---
description: 以標準使用者身分執行的應用程式會啟動排程工作，以執行需要系統管理員許可權的作業。
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: 提高許可權的工作模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320548"
---
# <a name="elevated-task-model"></a>提高許可權的工作模型

在提高許可權的工作模型中，以標準使用者身分執行的應用程式會藉由啟動排程工作來執行需要系統管理員許可權的作業。

**Windows Server 2003 和 WINDOWS XP：** 不支援提高許可權的工作模型。

工作不會耗用許多系統資源做為服務，而工作會在完成時自動關閉。 除非需要與舊版作業系統的回溯相容性，否則請考慮使用此模型，而不是 [作業系統服務模型](operating-system-service-model.md) 。

若要使用工作來執行標準使用者應用程式的特殊許可權作業，必須符合下列條件：

-   工作必須設定為以 **系統** 的形式執行。
-   與工作相關聯的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 必須設定為允許標準使用者啟動工作。
-   工作排程器服務必須正在執行。

如需有關如何建立和啟動工作的詳細資訊，請參閱 [工作排程器](/windows/desktop/TaskSchd/task-scheduler-start-page)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發需要系統管理員許可權的應用程式](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[系統管理員訊息代理程式模型](administrator-broker-model.md)
</dt> <dt>

[系統管理員 COM 物件模型](administrator-com-object-model.md)
</dt> <dt>

[作業系統服務模型](operating-system-service-model.md)
</dt> </dl>

 

 
