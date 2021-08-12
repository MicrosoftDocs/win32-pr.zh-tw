---
description: InkPicture. NewPackets 事件-當筆墨收集器收到封包時發生。
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: 'InkPicture. NewPackets 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11568d898bb6f152b5d430cf1f347390174c16a51b0572e45ddd3528c8e0dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451087"
---
# <a name="inkpicturenewpackets-event"></a>InkPicture. NewPackets 事件

當筆墨收集器收到封包時發生。

## <a name="syntax"></a>語法


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 [**NewInAirPackets**](inkpicture-newinairpackets.md)事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*筆觸* \[在\]
</dt> <dd>

[**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。

</dd> <dt>

*PacketCount* \[在\]
</dt> <dd>

針對 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件接收的封包數目。

</dd> <dt>

*PacketData* \[in、out\]
</dt> <dd>

陣列，其中包含所選取的封包資料。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

在收集筆劃時接收封包。 封包事件會快速發生，且 **NewPackets** 事件處理常式必須快速或效能受到影響。

此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICENewPackets 識別碼的) \_ 。

應謹慎使用這個事件，因為在事件處理常式中執行太多程式碼時，可能會對筆墨效能造成負面影響。

若要設定包含在此陣列中的屬性，請使用筆墨收集器物件的 [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) 屬性。 *PacketData* 參數傳回的陣列包含這些屬性的資料。

> [!Note]  
> 雖然您可以修改封包資料，但不會保存或使用這些修改。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**NewInAirPackets 事件**](inkpicture-newinairpackets.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




