---
description: 多工作業系統會將可用的處理器時間分割在需要它的進程或執行緒之間。
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: 多工
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319163"
---
# <a name="multitasking"></a>多工

多工作業系統會將可用的處理器時間分割在需要它的進程或執行緒之間。 系統是針對優先處理的多工而設計它會將處理器 *時間* 配量配置給它所執行的每個執行緒。 目前執行中的執行緒會在其時間配量過期時暫停，讓另一個執行緒執行。 當系統從某個執行緒切換至另一個執行緒時，會儲存佔用的執行緒內容，並還原佇列中下一個執行緒的已儲存內容。

時間配量的長短取決於作業系統和處理器。 由於每個時間配量都很小 (大約20毫秒的) ，因此多個執行緒會同時執行。 這實際上就是多處理器系統上的情況，其中會在可用的處理器之間分配可執行的執行緒。 但是，當您在應用程式中使用多個執行緒時，必須特別小心，因為如果有太多執行緒，系統效能可能會降低。

如需詳細資訊，請參閱下列主題：

-   [多工處理的優點](advantages-of-multitasking.md)
-   [使用多工的時機](when-to-use-multitasking.md)
-   [多工考慮](multitasking-considerations.md)

 

 



