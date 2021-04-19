---
title: SyncState 屬性
description: SyncState 屬性是32位值的字串表示，當它與可攜式裝置同步播放清單時，Windows Media Player 使用此值。
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- SyncState 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994606"
---
# <a name="syncstate-attribute"></a>SyncState 屬性

**SyncState** 屬性是32位值的字串表示，當它與可攜式裝置同步播放清單時，Windows Media Player 使用此值。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [其他專案](other-item-attributes.md)
-   [相片專案](photo-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性是由 16 2 位值所組成，每個值都會指定可攜式裝置的同步處理狀態。 此32位值 (MSB) 最重要的位會對應至裝置16。  (LSB) 相對於裝置1最不重要的位。

每個2位值的 MSB 會指出 Windows Media Player 是否與對應的裝置同步處理內容。 值為1表示它已完成。 值為0表示它不是。

如果 MSB 為0，則 LSB 會指定同步處理失敗的原因。 LSB 中的值為1，表示沒有足夠的可用空間來容納內容。 LSB 中的值為0，表示某些其他原因導致無法同步處理。

若要取得指定裝置的同步處理狀態，請執行下列動作：

1.  叫用 **IWMPSyncDevice：： get \_ 狀態** ，以判斷指定的裝置是否已同步處理。
2.  如果已同步處理，請叫用 **IWMPSyncDevice：： get \_ partnershipIndex** ，以在 **SyncState** 屬性中取得裝置位組的索引。
3.  使用這個索引，將 **SyncState** 屬性的對應位組加上遮罩，並檢查結果以判斷播放清單與裝置的同步處理狀態。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**判斷播放清單同步處理狀態**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice：： get \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**IWMPSyncDevice：： get \_ 狀態**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





