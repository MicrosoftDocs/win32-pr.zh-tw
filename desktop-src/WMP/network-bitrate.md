---
title: Network. 位元速率
description: 位元速率屬性會抓取目前接收的位速率。
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- 網路位元速率 Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec142885bdd718903e956f8e86b59c3753cb024ecccc5efb2f8494797ea6a818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901778"
---
# <a name="networkbitrate"></a>Network. 位元速率

**位元速率** 屬性會抓取目前接收的位速率。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**位元速率**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

此值是目前影片和音訊串流的位元速率組合。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**位元速率** 顯示目前的媒體位元速率。 這項資訊會顯示在以 ID = "BR" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

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
</dt> </dl>

 

 





