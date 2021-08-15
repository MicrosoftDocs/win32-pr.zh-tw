---
title: 附加到 SDO 電腦
description: 使用 CoCreateInstance 傳回的介面指標，呼叫 ISdoMachine 附加方法。
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5863302da3f213c1360c254782a31c0dfc4fcb9a946f5827155862bca01405cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362186"
---
# <a name="attaching-to-the-sdo-computer"></a>附加到 SDO 電腦

使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)傳回的介面指標，呼叫 [**ISdoMachine：： Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) 方法。 傳遞 **Null** 做為 **附加** 方法的參數。 **Null** 值指定 **Attach** 會將電腦物件與本機電腦建立關聯。 不支援附加至遠端電腦。

若要判斷本機電腦是否已連接，請呼叫 [**ISdoMachine：： GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) 方法。

請參閱 [附加至 SDO-Enabled 電腦](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) ，取得示範如何連接到本機電腦的範例程式碼。

 

 