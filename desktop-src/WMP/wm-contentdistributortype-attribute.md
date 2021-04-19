---
title: WM/ContentDistributorType 屬性
description: WM/ContentDistributorType 屬性是專案散發者的型別。
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- WM/ContentDistributorType 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977486"
---
# <a name="wmcontentdistributortype-attribute"></a>WM/ContentDistributorType 屬性

**WM/ContentDistributorType** 屬性是專案散發者的型別。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性的值將會設定為 "List" 或 "單選"。 這個屬性會儲存在文件庫和數位媒體檔案中。

**ContentDistributorType** 是此屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMContentDistributorType。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





