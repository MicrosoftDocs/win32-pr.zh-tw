---
description: 當佇列完成認可其作業之後，應該使用 SetupCloseFileQueue 函式搭配 SetupOpenFileQueue 建立的控制碼來關閉它。
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: 關閉檔案佇列和 INF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce5c81c75f7515acfb346b4277e416b0cb2c2a9be6e40464dcfdfc21c3b23bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887573"
---
# <a name="closing-the-file-queue-and-inf-file"></a>關閉檔案佇列和 INF 檔案

當佇列完成認可其作業之後，應該使用 [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) 函式搭配 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)建立的控制碼來關閉它。 預設佇列回呼必須終結並重新建立，然後才能認可另一個佇列。

如果預設內容已起始供預設回呼常式使用，則也應該透過呼叫 [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) 函式來終止。 *內容* 是 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)函數所傳回之結構的指標。

當不再需要存取 INF 資訊時，請使用 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)所建立的控制碼來呼叫 [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)函式，以釋放系統資源。

 

 



