---
description: 應用程式可以安全地使用 C 執行時間程式庫的記憶體管理功能 (malloc、free 等等) 和 c + + (new、delete 等) 。
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: 標準 C 程式庫函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972271"
---
# <a name="standard-c-library-functions"></a>標準 C 程式庫函式

應用程式可以安全地使用 C 執行時間程式庫的記憶體管理功能 (**malloc**、 **free** 等等) 和 c + + (**new**、 **delete** 等) 。 C 執行時間程式庫函式在16位 Windows 下沒有可能的問題。 記憶體管理不再是問題，因為系統可以在不影響虛擬位址的情況下，藉由移動實體記憶體的頁面來自由管理記憶體。 同樣地，接近和遠指標之間的差異不再相關。 因此，您可以使用標準 C 程式庫函數進行記憶體管理。 不過，記憶體管理函式確實提供了 C 執行時間程式庫中無法使用的功能。

 

 



