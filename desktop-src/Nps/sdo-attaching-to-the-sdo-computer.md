---
title: 附加到 SDO 電腦
description: 使用 CoCreateInstance 傳回的介面指標，呼叫 ISdoMachine 附加方法。
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933314"
---
# <a name="attaching-to-the-sdo-computer"></a>附加到 SDO 電腦

使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)傳回的介面指標，呼叫 [**ISdoMachine：： Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) 方法。 傳遞 **Null** 做為 **附加** 方法的參數。 **Null** 值指定 **Attach** 會將電腦物件與本機電腦建立關聯。 不支援附加至遠端電腦。

若要判斷本機電腦是否已連接，請呼叫 [**ISdoMachine：： GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) 方法。

請參閱 [附加至 SDO-Enabled 電腦](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) ，取得示範如何連接到本機電腦的範例程式碼。

 

 