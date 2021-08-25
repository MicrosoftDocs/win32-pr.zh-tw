---
description: 以標準使用者的形式執行的應用程式會使用遠端程序呼叫（ (RPC) ）與以系統執行的服務進行通訊。
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: 作業系統服務模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af797a7baad8390b1b4bc79fd7723a518c587ed58cc2dab27ab2898845335ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907798"
---
# <a name="operating-system-service-model"></a>作業系統服務模型

在作業系統服務模型中，以標準使用者的形式執行的應用程式會使用 [遠端程序呼叫](/windows/desktop/Rpc/rpc-start-page)（ (RPC) ）與以 **系統** 執行的服務進行通訊。

標準使用者應用程式會在應用程式資訊清單中標示為並無 requestedexecutionlevel **asInvoker**。 若要執行需要系統管理員許可權的作業，標準使用者應用程式會對服務提出要求。

作業系統服務模型的其中一種用途是管理可能會影響系統的應用程式，例如防毒軟體或其他垃圾軟體和間諜軟體。 標準使用者應用程式可讓登入的使用者控制服務的某些層面。 此服務負責判斷它針對標準使用者應用程式所執行的作業。 例如，防毒軟體服務可能會允許標準使用者啟動系統掃描，但可能不允許標準使用者停用即時病毒檢查。

使用作業系統服務模型的主要優點是不需要提高許可權提示。

使用作業系統服務模型的其中一個缺點，就是在系統上執行的服務所使用的資源比工作還多，而且標準使用者無法停止服務。 如果尾碼，請考慮使用 [提升許可權](elevated-task-model.md) 的工作模型。

若要執行作業系統服務模型，請建立標準使用者用戶端應用程式和作業系統服務。 在產品安裝期間，于作業系統中安裝此服務。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發需要系統管理員許可權的應用程式](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[系統管理員訊息代理程式模型](administrator-broker-model.md)
</dt> <dt>

[系統管理員 COM 物件模型](administrator-com-object-model.md)
</dt> <dt>

[提高許可權的工作模型](elevated-task-model.md)
</dt> </dl>

 

 
