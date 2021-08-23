---
title: 網路。頻寬
description: 頻寬屬性會抓取剪輯目前的頻寬。
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Network. 頻寬 Windows Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40bd97ae2efe7513bc69d308a29356cfc7b141ecc84b816bdc7fad68d79aa785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616875"
---
# <a name="networkbandwidth"></a>網路。頻寬

**頻寬** 屬性會抓取剪輯目前的頻寬。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**頻寬**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

如果 *播放玩家*，這個屬性會傳回零。未設定 **URL** 屬性。 這個屬性只對串流媒體有效。

## <a name="examples"></a>範例

下列 Microsoft JScript 範例會使用 *網路*。顯示目前媒體頻寬的 **頻寬**。 這項資訊會顯示在以 ID = "BW" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

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

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





