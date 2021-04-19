---
title: StretchToFit
description: StretchToFit 屬性會指定或抓取值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- StretchToFit Windows Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977407"
---
# <a name="playerstretchtofit"></a>StretchToFit

**StretchToFit** 屬性會指定或抓取值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。

## <a name="syntax"></a>Syntax

*玩家*。**stretchToFit**

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **布林值**。



| 值 | 描述                                            |
|-------|--------------------------------------------------------|
| true  | 影片將會延展以符合視窗。              |
| false | 預設值。 影片將不會延展以符合視窗。 |



 

## <a name="remarks"></a>備註

當 **stretchToFit** 設定為 true 時，Windows Media Player 控制項會維持影片的原始外觀比例。 如果影片的長寬比與影片視窗的外觀比例不相符，則可能會在影片影像的頂端和底部或左邊和右邊出現黑色遮罩區域。

只有當內嵌在網頁中時，此屬性才會套用至 Windows Media Player 控制項。

**Windows Media Player 10** 行動裝置版：不支援這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.1 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





