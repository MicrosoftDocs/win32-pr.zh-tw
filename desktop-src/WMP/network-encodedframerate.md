---
title: EncodedFrameRate
description: EncodedFrameRate 屬性會以每秒畫面格的畫面數來抓取內容作者所指定的影片畫面播放速率。
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- EncodedFrameRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f64b6f57b4cfd0e7bc94715f80c1066ebe23a601e64c173926cf2cd9e36393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901698"
---
# <a name="networkencodedframerate"></a>EncodedFrameRate

**EncodedFrameRate** 屬性會以每秒畫面格的畫面數來抓取內容作者所指定的影片畫面播放速率。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**encodedFrameRate**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**encodedFrameRate** 可顯示編碼檔案時所指定的畫面播放速率。 這項資訊會顯示在以 ID = "FR" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
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

[**Network. 幀**](network-framerate.md)
</dt> </dl>

 

 





