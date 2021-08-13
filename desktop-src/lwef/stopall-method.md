---
title: StopAll 方法
description: StopAll 方法
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b138be6ea75135d5ddefdea9e1e5cc120d875ae092478ad3147332720e5a0907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745940"
---
# <a name="stopall-method"></a>StopAll 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

停止指定字元的所有動畫要求或指定類型的要求。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。StopAll_ *  \[ *類型*\]



| 部分   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *類型* | 選擇性。 若要使用此參數，您可以使用下列任何一個值。 您也可以使用逗號分隔來指定多個類型。 <br/> "**Get**" <br/> 停止所有已排入佇列的 [**Get**](get-method.md) 要求。<br/> "**NonQueuedGet**" <br/> 若要停止所有非佇列的 [**get**](get-method.md) 要求 (**Get** 方法，並將 **Queue** 參數設定為 **False**) 。<br/> 「**移動**」 <br/> 停止所有已排入佇列的 [**MoveTo**](moveto-method.md) 要求。<br/> 「**播放**」 <br/> 停止所有已排入佇列的 [**播放**](play-method.md) 要求。<br/> 「**說話**」 <br/> 停止所有已排入佇列的 [**朗讀**](speak-method.md) 要求。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您未設定 **Type** 參數，伺服器會停止該字元的所有動畫，包括已排入佇列和非佇列的 [**Get**](get-method.md) 要求，並清除其動畫佇列。 它也會停止播放隱藏或顯示動畫的字元。

這個方法不會產生 [**Request**](/windows/desktop/lwef/the-request-object) 物件。

## <a name="see-also"></a>另請參閱

[**Stop 方法**](stop-method.md)


 

