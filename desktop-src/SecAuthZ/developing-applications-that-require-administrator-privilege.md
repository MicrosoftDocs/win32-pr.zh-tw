---
description: 您可以開發應用程式來執行需要系統管理員許可權，但以標準使用者身分執行的作業。
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: 開發需要系統管理員許可權的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dc8ea112cfec6297cf7c11a044e62695a24e93d7eb0b13a773d40acd6c6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994428"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>開發需要系統管理員許可權的應用程式

您可以開發應用程式來執行需要系統管理員許可權，但以標準使用者身分執行的作業。

有幾個模型可以完成這項程式。



| 主題                                                                | 描述                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [提高許可權的工作模型](elevated-task-model.md)                       | 以標準使用者身分執行的應用程式會啟動排程工作，以執行需要系統管理員許可權的作業。                                                                     |
| [作業系統服務模型](operating-system-service-model.md) | 以標準使用者的形式執行的應用程式會使用 [遠端程序呼叫](/windows/desktop/Rpc/rpc-start-page)（ (RPC) ）與以 **系統** 執行的服務進行通訊。                                              |
| [系統管理員訊息代理程式模型](administrator-broker-model.md)         | 應用程式分成兩個程式。 其中一個程式是以標準使用者身分執行，另一個則以系統管理員許可權執行。                                                          |
| [系統管理員 COM 物件模型](administrator-com-object-model.md) | 以標準使用者身分執行的應用程式會藉由建立提高許可權的 [元件物件模型](/windows/desktop/com/component-object-model--com--portal) 物件，執行需要系統管理員許可權的作業。 |



 

 

 
