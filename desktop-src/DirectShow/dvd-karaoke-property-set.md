---
description: 當 DVD 瀏覽器篩選進入 [卡拉 ok] 模式時，它會透過 AM \_ 屬性 \_ DVDKARAOKE ENABLE 屬性通知音訊解碼器 \_ 。
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: 'DVD 卡拉 Dvdmedia 屬性集 (.h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3f7674b240934ae7440858b7317fd1abaf9b7833e36f80d7edc6cc185bc932
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016016"
---
# <a name="dvd-karaoke-property-set"></a>DVD 卡拉卡拉屬性集

當 [DVD 流覽](dvd-navigator-filter.md) 器篩選進入 [卡拉 ok] 模式時，它會透過 **AM \_ 屬性 \_ DVDKARAOKE \_ ENABLE** 屬性通知音訊解碼器。 然後，此解碼器必須將音訊通道2到5靜音，直到它從 DVD 導覽器收到 am **\_ 屬性 \_ DVDKARAOKE \_ 資料** 屬性，並以 [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) 資料結構的指標指出如何混合輔助通道。



| 標籤 | 值 |
|-------------------|-----------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ DvdKaraoke |



 



| 屬性識別碼                      | 描述                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ 屬性 \_ DVDKARAOKE \_ 啟用 | 布林值。 DVD 導覽器會將 AM \_ 屬性 \_ DVDKARAOKE 啟用，並將值設為 \_ **TRUE** ，以啟用卡拉卡拉 downmixing 或 **FALSE** 來停用它。                                                                                                                                    |
| AM \_ 屬性 \_ DVDKARAOKE \_ 資料   | DVD 導覽器 \_ \_ 會以 \_ [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) 結構的指標傳送 DVDKARAOKE 資料屬性給解碼器，以變更 downmix 設定; 也就是，若要開啟或關閉特定的卡拉卡拉通道，並將其導向右邊或左輸出通道。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 




