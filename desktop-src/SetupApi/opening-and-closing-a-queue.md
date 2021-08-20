---
description: 您必須先開啟檔案佇列，才能將檔案作業排在佇列中。 呼叫 SetupOpenFileQueue 函數會傳回佇列檔案的控制碼。 後續的佇列函式會使用此控制碼來參考開啟的佇列，並對其新增作業或掃描它。
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: 開啟和關閉佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8465446842521adbd320816a76d7f545819eebf68b55aee0c3a057fc0ca3ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965151"
---
# <a name="opening-and-closing-a-queue"></a>開啟和關閉佇列

您必須先開啟檔案佇列，才能將檔案作業排在佇列中。 呼叫 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) 函數會傳回佇列檔案的控制碼。 後續的佇列函式會使用此控制碼來參考開啟的佇列，並對其新增作業或掃描它。

所有指定的檔案作業都已排入佇列並認可之後，您必須呼叫 [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) 函式來釋放在呼叫 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)時所配置的資源。

> [!Note]  
> [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)函數不會認可檔案佇列。 呼叫 **SetupCloseFileQueue** 時未認可的任何作業都不會執行。

 

 

 



