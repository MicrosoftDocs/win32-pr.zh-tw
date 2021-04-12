---
description: 除了個別佇列檔案作業之外，您也可以將 INF 區段中所列的所有檔案排入佇列。
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: 將 INF 區段排入佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513845"
---
# <a name="queuing-an-inf-section"></a>將 INF 區段排入佇列

除了個別佇列檔案作業之外，您也可以將 INF 區段中所列的所有檔案排入佇列。

您可以藉由呼叫 [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)，將 INF 檔案的 [**複製** 檔案] 區段中所列的所有檔案排入佇列。 若要讓此函式成功，[ **複製** 檔案] 區段必須是正確的格式，而 INF 檔案或其中一個附加的檔案必須包含 **SourceDisksFiles** 和 **SourceDisksNames** 區段。

同樣地，如果您想要刪除 INF 檔案的 [ **刪除** 檔案] 區段中指定的所有檔案，您可以呼叫 [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)。 若要重新命名 INF 檔案中 [ **重新命名** 檔案] 區段中的所有檔案，請使用 [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)。

 

 



