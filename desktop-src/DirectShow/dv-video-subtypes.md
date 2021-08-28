---
description: 針對 DV 影片定義了許多子類型。 每個都有 FOURCC 碼和對應的 GUID 值。 並非所有這些格式都受到支援;如需詳細資訊，請參閱「備註」一節。
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: 'DV 影片子類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ee08bad5970d016ada2bf129132bf34261be9ba856071d9f90f1e73de91978
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102948"
---
# <a name="dv-video-subtypes"></a>DV 影片子類型

針對 DV 影片定義了許多子類型。 每個都有 FOURCC 碼和對應的 GUID 值。 並非所有這些格式都受到支援;如需詳細資訊，請參閱「備註」一節。

## <a name="consumer-formats"></a>取用者格式



| FOURCC | GUID               | 資料速率 | 描述                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | MEDIASUBTYPE \_ dvsl | 12.5 Mbps | SD-DVCR (525-60 或 625-50)    |
| 'dvsd' | MEDIASUBTYPE \_ dvsd | 25 Mbps   | SDL-DVCR (525-60 或 625-50)   |
| 'dvhd' | MEDIASUBTYPE \_ dvhd | 50 Mbps   | HD-DVCR (1125-60 或 1250-50)  |



 

如需這些格式的詳細資訊，請參閱 IEC-61834。

## <a name="professional-formats"></a>Professional格式



| FOURCC | GUID               | 資料速率 | 描述                                 |
|--------|--------------------|-----------|---------------------------------------------|
| 'dv25' | MEDIASUBTYPE \_ dv25 | 25 Mbps   | DVCPRO 25 (525-60 或 625-50) 。               |
| 'dv50' | MEDIASUBTYPE \_ dv50 | 50 Mbps   | DVCPRO 50 (525-60 或 625-50)                 |
| 'dvh1' | MEDIASUBTYPE \_ dvh1 | 100 Mbps  | DVCPRO 100 (1080/60i、1080/50i 或 720/60P)  |



 

如需有關 dv25 和 dv50 的詳細資訊，以及有關 dvh1 的詳細資訊，請參閱 [SMPTE] 314M。

## <a name="miscellaneous"></a>其他

標頭檔 Uuid 中定義了兩個額外的 DV 子類型。 這些會對應至特定 DV 編解碼器所產生的 FOURCC 碼;它們不會對應至任何定義的 DV 標準。 這些子類型已淘汰，不應該使用。



| FOURCC | GUID               |
|--------|--------------------|
| DVCS | MEDIASUBTYPE \_ DVCS |
| 'DVSD' | MEDIASUBTYPE \_ DVSD |



 

## <a name="remarks"></a>備註

下表顯示 MSDV 和 UVC 驅動程式支援的資料速率（以每秒 mb 數為單位） (Mbps) 。



| 作業系統                                                                 | MSDV (IEEE 1394) 驅動程式 | UVC 驅動程式    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| WindowsXP Service Pack 1 或更早版本                                             | 12.5、25                | 無法使用 |
| WindowsXP Service pack 2 或更新版本，Windows Server 2003 Service pack 1 或更新版本。 | 12.5、25、50、100       | 12.5、25      |



 

若為 25 mbps 的串流，MSDV 驅動程式在 Windows Vista 之前 Windows Vista 中的行為已變更，MSDV 驅動程式一律會將媒體類型設定為 \_ 25-Mbps 串流的 MEDIASUBTYPE dvsd，不論來源是否為 SDL-DVCR 或 DVCPRO 25。 未使用 ' dv25 ' 媒體類型。 從 Windows Vista 開始，MSDV 驅動程式現在會區分這兩種格式。 針對 SDL DVCR，它會繼續使用 ' dvsd ' 子類型。 針對 DVCPRO 25，它現在會使用 ' dv25 ' 子類型。

DirectShow [dv 分隔](dv-splitter-filter.md)器和[DV 影片解碼](dv-video-decoder-filter.md)篩選器只支援 SDL DVCR 格式。 資料可以是 PAL 或 NTSC。 您可以使用協力廠商篩選或編解碼器來剖析其他 DV 格式，只要 MSDV 或 UVC 驅動程式支援資料速率即可。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[MSDV 驅動程式](msdv-driver.md)
</dt> <dt>

[影片子類型](video-subtypes.md)
</dt> </dl>

 

 




