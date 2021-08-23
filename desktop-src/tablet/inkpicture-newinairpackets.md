---
description: InkPicture. NewInAirPackets 事件-當出現無線封包時，就會發生此事件。
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: 'InkPicture. NewInAirPackets 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f81f6f485329eaa5cd96c2aece39646e700a21bc762c5d66344e5daf0a628f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967047"
---
# <a name="inkpicturenewinairpackets-event"></a>InkPicture. NewInAirPackets 事件

當出現無線封包時發生。

## <a name="syntax"></a>語法


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **NewInAirPackets** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*PacketCount* \[在\]
</dt> <dd>

收到的無線封包數目。

</dd> <dt>

*PacketData* \[in、out\]
</dt> <dd>

陣列，其中包含所選取的封包資料。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當使用者將畫筆移近 tablet，而游標位於筆墨收集器物件的視窗內，或使用者在筆跡收集器物件的相關視窗內移動滑鼠時，就會建立無線封包。 **NewInAirPackets** 事件會快速產生，而事件處理常式必須快速或效能受到影響。

此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICENewInAirPackets 識別碼的) \_ 。

即使在選取或清除模式下，也不只是在插入筆墨時，也會引發 **NewInAirPackets** 事件。 這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。 這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。

若要設定包含在此陣列中的屬性，請使用筆墨收集器物件的 [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) 屬性。 *PacketData* 參數傳回的陣列包含這些屬性的資料。

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

[**DesiredPacketDescription 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[**NewPackets 事件**](inkpicture-newpackets.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




