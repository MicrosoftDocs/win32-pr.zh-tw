---
title: Show 方法
description: Show 方法
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965640"
---
# <a name="show-method"></a>Show 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

使指定的字元可見，並播放其相關聯的 **顯示** 動畫。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" 的字元 ) 。顯示* *  \[ *快速*\]



| 部分   | 描述                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *快速* | 選擇性。 指定伺服器是否會播放 **顯示** 動畫的布林運算式。 **True** 略過 **顯示** 狀態動畫。 <br/> **False** (預設) 不會略過 **顯示** 狀態動畫。 <br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 此外，如果關聯的 **顯示** 動畫尚未載入，而且您尚未將 **Fast** 參數指定為 **True**，則伺服器會將 **要求** 物件的 [**Status**](status-property.md) 屬性設為「失敗」，並提供適當的錯誤號碼。 因此，如果您使用 HTTP 通訊協定來存取字元動畫資料，請在呼叫 **Show** 方法之前，使用 [**Get**](get-method.md)方法載入 **顯示** 狀態動畫。

避免將 **Fast** 參數設定為 **True** ，而不先事先播放動畫;否則，字元框架可能不會顯示任何影像。 尤其要注意的是，如果您在字元未顯示時呼叫 [**MoveTo**](moveto-method.md) ，則不會播放任何動畫。 因此，如果您以 **Fast** 設定為 **True** 來呼叫 **Show** 方法，則不會顯示任何影像。 同樣地，如果您呼叫 [[**隱藏**](hide-method.md)]，並將 [**快速****顯示**] 設定為 [ **True**]，就不會有可見的影像。

## <a name="see-also"></a>另請參閱

[**Hide 方法**](hide-method.md)


 

