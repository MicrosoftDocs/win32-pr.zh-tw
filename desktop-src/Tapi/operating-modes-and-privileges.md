---
description: 開啟手機裝置時，應用程式可以要求兩種作業模式的其中一種。
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: 操作模式和許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f7d3c1f6b7049c3986b96734a537906dc62166c48d62e549684cdaa6d35ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012468"
---
# <a name="operating-modes-and-privileges"></a>操作模式和許可權

開啟手機裝置時，應用程式可以要求兩種作業模式的其中一種。 這些模式反映應用程式要求裝置的許可權：

-   開啟監視許可權的電話可讓應用程式判斷電話裝置的狀態。 當偵測到電話裝置上的狀態變更時，會將訊息傳送至應用程式。
-   開啟手機裝置以取得擁有者許可權的應用程式，可以使用可修改電話裝置狀態的作業。 擁有者許可權也會自動包含完整的監視器許可權。 在任何時間，指定的電話裝置只能針對擁有者許可權開啟一次，但有多次用於監視許可權。 所有的 **phoneSet** 作業都需要擁有者許可權，而所有 **phoneGet** 作業只需要監視許可權。

 

 



