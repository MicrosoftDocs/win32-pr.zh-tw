---
description: 如果專家在執行時間失敗，如果您使用網路監視器函式進行記憶體管理，網路監視器將會釋放配置的記憶體。
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: 管理記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943517"
---
# <a name="managing-memory"></a>管理記憶體

如果專家在執行時間失敗，如果您使用網路監視器函式進行記憶體管理，網路監視器將會釋放配置的記憶體。 但是，當您撰寫專家時，可能需要取得系統資源和資料結構資訊。 例如，網路監視器通訊協定聯合專家會取得檔案控制代碼來建立新的捕獲。 每個專家都必須建立自己的 **try/catch** 處理，讓專家可以釋出所取得的資源。

配置記憶體時，請使用下列現有的記憶體函數：

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



