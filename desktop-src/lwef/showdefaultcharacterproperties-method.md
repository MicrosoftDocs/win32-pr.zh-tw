---
title: ShowDefaultCharacterProperties 方法
description: ShowDefaultCharacterProperties 方法
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d19f92f555038fe4c13c7a752d49bf35a04b70964f6110d881976af3e72a8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746304"
---
# <a name="showdefaultcharacterproperties-method"></a>ShowDefaultCharacterProperties 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

顯示預設字元的屬性。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 * * *。ShowDefaultCharacterProperties* *  \[ *X* 、 *Y*\]



| 部分 | 描述                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | 選擇性。 指出水準 (*X* ) 螢幕座標以顯示視窗的短整數值。 此座標必須以圖元為單位來指定。 |
| *Y*  | 選擇性。 表示垂直 (*Y*) 螢幕座標以顯示視窗的短整數值。 此座標必須以圖元為單位來指定。    |



 

</dd> </dl>

## <a name="remarks"></a>備註

呼叫這個方法會顯示預設的 [字元屬性] 視窗 (不是 [Microsoft 代理程式] 屬性工作表) 。 如果您未指定 X 和 Y 座標，視窗會出現在最後一個顯示的位置。

## <a name="see-also"></a>另請參閱

[**DefaultCharacterChange 事件**](defaultcharacterchange-event.md)


 

 




