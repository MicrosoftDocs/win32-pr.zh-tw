---
description: 藉由呼叫 SetupOpenFileQueue 函式取得檔案佇列的控制碼之後，您可以將檔案作業新增至佇列（依檔案的方式），或將所有檔案排入 INF 區段中的所有檔案。
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: 佇列檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849442"
---
# <a name="queuing-files"></a>佇列檔

藉由呼叫 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) 函式取得檔案佇列的控制碼之後，您可以將檔案作業新增至佇列（依檔案的方式），或將所有檔案排入 INF 區段中的所有檔案。

若要在檔案佇列中加入個別檔案的複製作業，請呼叫 [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) 函式。 如果您想要使用 INF 檔案中指定的預設來源媒體和目標目的地來將檔案複製作業排入佇列，您可以呼叫 [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) 函式。

您可以藉由呼叫 [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) 或 [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) 函數，將個別檔案刪除或重新命名作業新增至開啟的檔案佇列。

 

 



