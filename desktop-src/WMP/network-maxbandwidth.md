---
title: MaxBandwidth
description: MaxBandwidth 屬性會指定或抓取允許的最大頻寬。
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- MaxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986164"
---
# <a name="networkmaxbandwidth"></a>MaxBandwidth

**MaxBandwidth** 屬性會指定或抓取允許的最大頻寬。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**maxBandwidth**

## <a name="possible-values"></a>可能的值

這個屬性是 (**長**) 的讀取/寫入 **號碼**。

## <a name="remarks"></a>備註

此屬性沒有預設值。 當 Windows Media Player 現正播放時，可以指定其值，但在目前的媒體專案發行之前，只要開啟另一個媒體專案或呼叫 *Player*，變更就不會生效。**關閉**。 Windows Media Player 嘗試達到可能的最高頻寬。 只有在設定值的情況下，才會減少任何頻寬。

這項設定有助於減少使用的頻寬量，特別是在多位元率 (MBR) 串流的情況下。 MBR 資料流程包含多個具有不同位速率的資料流程。 在某些情況下，您可能會想要使用比用戶端所需的位元速率低的資料流程。 在此情況下，設定 **maxBandwidth** 屬性將會選取較低的位元速率串流。

例如，MBR 串流可能包含以每秒 20 kb 編碼的資料流程 (Kbps) 、37 Kbps 和 200 Kbps。 將 **maxBandwidth** 屬性設定為 50000 (50 Kbps) 將會選取 37 kbps 資料流程，而不是 200 kbps 串流。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> <dt>

[**Player. 關閉**](player-close.md)
</dt> </dl>

 

 





