---
title: WM/Set-protectiontype 屬性
description: WM/Set-protectiontype 屬性是在內容上使用的保護類型。
ms.assetid: aab36b57-5b4e-4a3f-80cf-872ec8369c49
keywords:
- WM/Set-protectiontype 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProtectionType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7888273aaca38a4fb87c5a19fc7c7bc8d47b13a8b6a03a578354b1a8bcd2b3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900348"
---
# <a name="wmprotectiontype-attribute"></a>WM/Set-protectiontype 屬性

**WM/set-protectiontype** 屬性是在內容上使用的保護類型。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

**Set-protectiontype** 是此屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMProtectionType。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





