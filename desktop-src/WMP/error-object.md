---
title: " (WMP SDK) 的 Error 物件"
description: Error 物件提供 ErrorItem 物件集合的存取權。
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Error 物件 Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8e5b7627db2c55eb41a267f6c8d3a7a779e2f20190ca3061a49a41eb8577adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748467"
---
# <a name="error-object"></a>Error 物件

**Error** 物件提供 [ErrorItem](erroritem-object.md)物件集合的存取權。

**Error** 物件支援下列屬性。



| 屬性                           | 描述                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | 捕獲錯誤佇列中的錯誤數目。 |



 

**Error** 物件支援下列方法。



| 方法                                       | 描述                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | 清除錯誤佇列中的錯誤。                                                         |
| [item](error-item.md)                       | 從錯誤佇列中捕獲 [ErrorItem](erroritem-object.md) 物件。                     |
| [webHelp](error-webhelp.md)                 | 啟動 Windows Media Player 的 Web 說明頁，以顯示有關錯誤的進一步資訊。 |



 

您可以透過下列屬性來存取 **Error** 物件。



| Object                      | 屬性                  |
|-----------------------------|---------------------------|
| [球員](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




