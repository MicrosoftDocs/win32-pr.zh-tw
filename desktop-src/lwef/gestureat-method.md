---
title: GestureAt 方法
description: GestureAt 方法
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462988"
---
# <a name="gestureat-method"></a>GestureAt 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

在指定的位置播放指定字元的 gesturing 動畫。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" 的字元 ) 。GestureAt* *  *x、y*



| 部分  | 描述                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x、y* | 必要。 整數值，指出字元將手勢的水準 (*x*) 螢幕座標和垂直 (*y*) 螢幕座標。 這些座標必須以圖元為單位來指定。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

伺服器會自動播放適當的動畫以朝指定的位置進行手勢。 座標一律相對於螢幕原點 (左上) 。

如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 此外，如果尚未在本機電腦上載入相關聯的動畫，伺服器會將 **要求** 物件的 [ [**狀態**](status-property.md) ] 屬性設定為 [失敗]，並提供適當的錯誤號碼。 因此，如果您使用 HTTP 通訊協定來存取字元動畫資料，請在呼叫 **GestureAt** 方法之前，使用 [**Get**](get-method.md)方法載入 **Gesturing** 狀態動畫。

 

 