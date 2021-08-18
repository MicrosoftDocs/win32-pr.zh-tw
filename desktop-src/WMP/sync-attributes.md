---
title: 同步屬性
description: Sync01 至 Sync16 屬性是32位值的字串表示，當它與多達16部可攜式裝置的其中一個同步播放清單時，Windows Media Player 會使用這些值。
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- 同步屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e720598b17db6b073524d80afc8f39dd6e6f87e777246b5bdb60294b161fa1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134751"
---
# <a name="sync-attributes"></a>同步屬性

**Sync01** 至 **Sync16** 屬性是32位值的字串表示，當它與多達16部可攜式裝置的其中一個同步播放清單時，Windows Media Player 會使用這些值。

## <a name="applies-to"></a>套用至

-   [播放清單](playlist-attributes-ref.md)

## <a name="remarks"></a>備註

這些都是讀取/寫入屬性。 值為零表示 Windows Media Player 不應該與相關聯的裝置同步播放清單。 大於零的值表示指定播放清單的同步處理優先權。

根據使用者輸入，Windows Media Player 會為文件庫中的每個播放清單設定這個屬性。 當 Windows Media Player 嘗試同步播放播放清單與可攜式裝置時，它會檢查每個播放清單來比較代表裝置合作關係的 **同步**_XX_ 屬性值。 具有較低 **同步**_XX_ 值的播放清單會獲得較高的同步處理優先權。

例如，程式庫可能包含下列四個播放清單和個別的 **同步**_XX_ 值：



| 播放清單名稱 | Sync01 值 |
|---------------|--------------|
| GymMusic. .WPL  | 0x0000000D   |
| 放寬 .WPL     | 0x00000020   |
| DriveHome. .WPL | 0x00000001   |
| NoGo. .WPL      | 0x00000000   |



 

當 Windows Media Player 同步處理與屬性相關聯的裝置時，它會以下列順序同步處理播放清單：

1.  DriveHome. .WPL
2.  GymMusic. .WPL
3.  放寬 .WPL

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**列舉同步播放清單**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





