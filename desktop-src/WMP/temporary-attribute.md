---
title: 暫存屬性
description: 暫存屬性指定播放清單是否為暫時性。
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- 暫存屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984294"
---
# <a name="temporary-attribute"></a>暫存屬性

**暫存** 屬性指定播放清單是否為暫時性。

**備註**

如果您從程式庫中取出播放清單，則對播放清單所做的變更會反映在使用者的程式庫中。 若要避免這種情況，請呼叫 [IWMPPlaylist：： setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) 傳遞屬性名稱 "暫時性" 和值 "true"。 這會將您的播放清單實例轉換成暫時的播放清單，在不變更原始播放清單的情況下，可以安全地進行編輯。

**適用於**

-   [播放清單](playlist-attributes-ref.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





