---
description: 剪輯會 epecifies 媒體來源。
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: 剪切元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b94ffdbd3d9b49d961cdefdd64de9a212858c5da4859c3beddb77db0ab732d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655512"
---
# <a name="clip-element"></a>剪切元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`clip`Epecifies 媒體來源。

## <a name="attributes"></a>屬性

[**clsid**](clsid-attribute.md)、 [**畫面播放速率**](framerate-attribute.md)、 [**鎖定**](lock-attribute.md)、 [**mlength**](mlength-attribute.md)、 [**mstart**](mstart-attribute.md)、 [**mstop**](mstop-attribute.md)、 [**靜音**](mute-attribute.md)、 [**src**](src-attribute.md)、 [**start**](start-attribute.md)、 [**stop**](stop-attribute.md)、 [**stream**](stream-attribute.md)、 [**stretchmode**](stretchmode-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



| 標籤 | 值 |
|----------|----------------------------------|
| 父代   | [**跟蹤**](track-element.md)   |
| Children | [**影響**](effect-element.md) |



 

## <a name="remarks"></a>備註

**Clsid** 屬性會指定來源篩選器的 clsid 作為來源使用。 請勿在相同元素內指定 **src** 和 **clsid** 屬性 `clip` 。

請至少指定 **一個開始或 mstart)  (開始** 或 ，以及 (**停止** 或 **mstop**) 的一個停止時間屬性。 如果未指定其中一個啟動時間屬性，它會預設為 0 (**開始** 的時間軸開頭，或 **mstart**) 的剪輯開頭。 如果未指定其中一個停止時間屬性，DES 會假設正常播放速率，並據此計算未指定的停止時間。 如果同時指定了兩個停止時間，如有需要，播放速度會比正常播放更快或更慢。

在下列範例中，時間軸持續時間是七秒 (**停止** 減去 **開始**) 。 假設採用正常播放速率，所以 media 停止時間預設為10秒， (持續時間加上 **mstart**) 。


```
<clip start="2" stop="9" mstart="3" />
```



在下一個範例中，媒體開始時間預設為0，強制媒體持續時間為10秒。 時間軸的持續時間為五秒，因此剪輯會以一般速率的兩倍播放回來。


```
<clip start="5" stop="10" mstop="10" />  
```



如果 **src** 屬性指定了靜止影像，DES 會嘗試載入一連串的靜止影像來建立動畫。 例如，如果 IMAGE001.BMP **src** 屬性，DES 會尋找 IMAGE002.BMP、IMAGE003.BMP、IMAGE004.BMP 等。 如果存在，則會依 **幀** 速率屬性所指定的速率，以連續的數位順序顯示。

## <a name="examples"></a>範例


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 



