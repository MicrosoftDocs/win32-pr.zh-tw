---
description: 建立 INF 檔案之後，您通常會為安裝應用程式撰寫原始程式碼。 您可以從安裝應用程式呼叫安裝程式函數，以執行許多安裝作業。
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: 建立安裝程式應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77f920a024a4414690baad7684af90a30ee4ca3c9f96a2c6f61b1b84430c072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887435"
---
# <a name="creating-setup-applications"></a>建立安裝程式應用程式

建立 INF 檔案之後，您通常會為安裝應用程式撰寫原始程式碼。 您可以從安裝應用程式呼叫安裝程式函數，以執行許多安裝作業。

下列步驟說明使用安裝函式來建立安裝程式的一種方式。 您可以使用此範例作為起點，或開發您自己的安裝演算法。

**初始 化**

-   [開啟 INF，並在適當的情況下附加其他 INF 檔案。](opening-the-inf-file.md)
-   [從 INF 檔案解壓縮檔案資訊。](extracting-file-information-from-the-inf-file.md)
-   [收集使用者的設定資訊。](gathering-setup-information-from-the-user.md)
-   [建立佇列。](creating-a-queue-and-queuing-file-operations.md)

**安裝檔案**

-   [認可佇列，並指定回呼常式。](committing-the-queue.md)
-   [更新登錄資訊。](updating-registry-information.md)

**清理**

-   [關閉檔案佇列和 INF。](closing-the-file-queue-and-inf-file.md)
-   [釋放任何其他系統資源並結束程式。](releasing-other-system-resources.md)

 

 



