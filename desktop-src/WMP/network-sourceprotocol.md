---
title: SourceProtocol
description: SourceProtocol 屬性會抓取用來接收資料的來源通訊協定。
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- SourceProtocol Windows Media Player
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998756"
---
# <a name="networksourceprotocol"></a>SourceProtocol

**SourceProtocol** 屬性會抓取用來接收資料的來源通訊協定。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**sourceProtocol**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

從 CD 或 DVD 播放媒體時，這個屬性會設定為 "" (空白字串) 。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**sourceProtocol** ，以顯示用來接收資料的來源通訊協定。 這項資訊會顯示在以 ID = "SP" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> </dl>

 

 





