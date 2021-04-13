---
description: 啟用來源讀取器的影片處理。
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: 'MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468989"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 影片 \_ 處理屬性

啟用 [來源讀取器](source-reader.md)的影片處理。

## <a name="data-type"></a>資料類型

**UINT32**



| 值                                                                                                                                                                | 意義                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**零**</dt> </dl> | 啟用影片處理。<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**零個**</dt> </dl>             | 停用影片處理。 (預設值)<br/> |



 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

如果此屬性為 **TRUE** (非零) ，來源讀取器可以在未壓縮的影片畫面上執行下列有限的影片處理：

-   從 YUV 轉換成 RGB-32。
-   去交錯.

這些作業是在軟體中執行，並不會針對播放進行優化。 這項功能適用于處理少量框架的應用程式（例如，建立影片縮圖），或是不會即時解碼框架的應用程式。 進行逐行壓縮作業時，會從單一欄位中插入資料，因此會有遺失的資料。

如果您使用 Direct3D 來顯示影片畫面，請避免此設定，因為 GPU 通常會提供更好的影片處理功能。

如果此屬性為 **TRUE**，則下列屬性必須為 **FALSE**：

-   [MF \_ 來源 \_ 讀取器 \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md)
-   [MF \_ READWRITE \_ 停用 \_ 轉換器](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> </dl>

 

 




