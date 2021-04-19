---
title: ErrorItem 物件
description: ErrorItem 物件提供存取錯誤資訊的方法。
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- ErrorItem 物件 Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966833"
---
# <a name="erroritem-object"></a>ErrorItem 物件

**ErrorItem** 物件提供存取錯誤資訊的方法。

**ErrorItem** 物件支援下列屬性。



| 屬性                                           | 描述                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [條件](erroritem-condition.md)               | 抓取指出錯誤條件的值。                                       |
| [customUrl](erroritem-customurl.md)               | 抓取網站的 URL，該網站會顯示有關編解碼器下載失敗的特定資訊。 |
| [errorCode](erroritem-errorcode.md)               | 抓取目前的錯誤碼。                                                               |
| [errorCoNtext](erroritem-errorcontext.md)         | 捕獲指出錯誤內容的值。                                          |
| [errorDescription](erroritem-errordescription.md) | 捕獲錯誤的描述。                                                           |
| **補救**                                         | 保留供未來使用。                                                                        |



 

**ErrorItem** 物件是透過下列方法來存取。



| Object                    | 方法                   |
|---------------------------|--------------------------|
| [錯誤](error-object.md) | [item](error-item.md)   |
| [媒體](media-object.md) | [error](media-error.md) |



 

例如，*播放* 程式的用途。*錯誤*。參考語法區段中會使用 (*索引*) 的 *專案*。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




