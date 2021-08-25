---
title: EAP 實行詳細資料
description: 存取點 (Ap) ，例如遠端存取服務 (RAS) 、使用必須由協力廠商 EAP DLL 匯出的函式呼叫來與 EAP 執行互動。
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8772d839e6d6fb748f56de0329a958057400d37afeb92a2f3ec89b3ab462e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852408"
---
# <a name="eap-implementation-details"></a>EAP 實行詳細資料

存取點 (Ap) ，例如遠端存取服務 (RAS) 、使用必須由協力廠商 EAP DLL 匯出的函式呼叫來與 EAP 執行互動。 換句話說，EAP 是提供者 API，這表示外掛程式或 Dll 會將程式碼實作為 EAP 提供者，但不能自行呼叫 EAP Api。 例如，EAP DLL 的程式設計人員會建立 EAP 初始化常式的程式碼，並將此程式碼放入 EAP 預先定義的函式 [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85))中。 然後，在執行時間，AP 連接管理員會呼叫包含程式碼的 **RasEapInitialize** 函式，以初始化 EAP 執行。

下列主題將詳細說明此互動：

-   [EAP 的存取點初始化](ras-initialization-of-eap.md)
-   [驗證通訊協定初始化](authentication-protocol-initialization.md)
-   [存取點和驗證通訊協定互動](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [完成驗證會話](completion-of-the-authentication-session.md)

 

 