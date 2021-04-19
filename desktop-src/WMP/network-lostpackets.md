---
title: LostPackets
description: LostPackets 屬性會捕獲遺失的封包數目。
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- LostPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997697"
---
# <a name="networklostpackets"></a>LostPackets

**LostPackets** 屬性會捕獲遺失的封包數目。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**lostPackets**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

這個屬性僅適用于串流媒體，而且在使用 HTTP 通訊協定（不失真）時，將會等於零。

封包可能因為許多原因而遺失，例如網路連線的類型和品質。

每次播放都會停止並重新啟動，這個屬性會設定為零。 如果播放暫停並重新啟動，則不會重設。 這個屬性只有在執行時間才會傳回有效的資訊，而且只有在 *播放玩家* 時才會傳回。已設定 **URL** 屬性。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**lostPackets** 可顯示當使用者按一下按鈕時，播放時遺失的封包總數。 這項資訊會顯示在以 ID = "LP" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

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

 

 





