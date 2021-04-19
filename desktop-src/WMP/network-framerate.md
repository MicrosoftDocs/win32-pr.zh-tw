---
title: Network. 幀
description: '[畫面播放速率] 屬性會以每數百秒的畫面格速率抓取目前的影片畫面速率。 例如，值2998表示每秒29.98 個畫面格。'
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- 網路. 幀 Windows Media Player
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989862"
---
# <a name="networkframerate"></a>Network. 幀

[ **幀** 速率] 屬性會以每數百秒的畫面格速率抓取目前的影片畫面速率。 例如，值2998表示每秒29.98 個畫面格。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**畫面播放速率**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。顯示目前畫面播放速率的 **幀** 速率。 這項資訊會顯示在以 ID = "FR" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
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
</dt> <dt>

[**EncodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





