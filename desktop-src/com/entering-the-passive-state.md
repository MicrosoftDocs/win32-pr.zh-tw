---
title: 進入被動狀態
description: 進入被動狀態
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a0a3a93b0ff0bd1c16701c82f271847ee435375112a8e7a03120155928fe1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736852"
---
# <a name="entering-the-passive-state"></a>進入被動狀態

物件關閉會強制內嵌或連結化物件進入被動狀態。 它通常是從 OLE 伺服器應用程式的使用者介面起始，例如當使用者選取 [關閉] 命令時。 在此情況下，OLE 伺服器應用程式會通知容器，它會釋放物件的參考計數。 當物件的所有參考都已釋放時，就可以釋出物件。 釋放所有物件時，可以安全地終止 OLE 伺服器應用程式。

容器應用程式也可以起始物件關閉。 若要關閉物件，容器會在完成選擇性儲存作業之後釋放其參考計數。 您可以將容器設計成在就地啟用會話之後停用物件時釋出物件，讓使用者可以在物件外部按一下，而不會遺失使用中的編輯會話。

 

 




