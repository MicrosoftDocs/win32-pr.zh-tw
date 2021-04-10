---
title: 現用屬性
description: 現用屬性
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183499"
---
# <a name="active-property"></a>現用屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回您的應用程式是否為字元的作用中用戶端，以及字元是否最上層。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式。***字元 * **** * * (」CharacterID * * * ) 。* 作用中 *  \[  =  *狀態*\]



| 部分    | 描述                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | 整數運算式，指定用戶端應用程式的狀態。 0不是作用中的用戶端。<br/> 1個作用中用戶端。 <br/> 2輸入-主動用戶端。  (最上方的字元。 ) <br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control [**Click**](click-event.md) 或 [DragStart](dragstart-event.md) events) 。 同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收命令事件。

您可以使用 [**啟動**](activate-method.md)方法來設定您的應用程式是字元的作用中用戶端，還是讓您的應用程式成為輸入使用中的用戶端 (也會讓字元) 最上層。

## <a name="see-also"></a>另請參閱

[啟動 * * 方法 * *](activate-method.md)


 

 





