---
description: 下列單字常數形成一組有效的 Windows 映像取得 (WIA) 相機專案屬性。
ms.assetid: 708f35e7-3ce4-4a9e-8547-2e12b6f535b2
title: '攝影機 WIA 專案屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPC_THUMBNAIL
- WIA_IPC_THUMB_WIDTH
- WIA_IPC_THUMB_HEIGHT
- WIA_IPC_AUDIO_AVAILABLE
- WIA_IPC_AUDIO_DATA_FORMAT
- WIA_IPC_AUDIO_DATA
- WIA_IPC_NUM_PICT_PER_ROW
- WIA_IPC_SEQUENCE
- WIA_IPC_TIMEDELAY
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 86df16c66064fe3c4502791b654d9f2c6a19219b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971222"
---
# <a name="camera-wia-item-property-constants"></a>攝影機 WIA 專案屬性常數

下列 **單字** 常數形成一組有效的 Windows 映像取得 (WIA) 相機專案屬性。

> [!Note]  
> WIA 不支援 Windows Vista 或更新版本中的相機。 針對這些版本的 Windows，請使用 Windows 驅動程式開發工具組中所述的 Windows 可攜式裝置 (WPD) API (DDK) 從相機取得映射。

 

前置詞 "WIA \_ IPC \_ " 表示攝影機的專案屬性，而且是 C/c + + 中使用的命名慣例。 針對腳本用途，這些常數會使用前置詞 "CameraPicture"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。



| 常數/值                                                                                                                                                                                                                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_IPC_THUMBNAIL"></span><span id="wia_ipc_thumbnail"></span><dl> <dt>**WIA \_IPC \_ 縮圖**</dt> <dt>CameraPictureThumbnail</dt> </dl>                                 | 包含每圖元24位的縮圖資料位。 迷你驅動程式會建立並 maintanis 此屬性。<br/> 這個屬性所包含的縮圖資料必須在未壓縮的點陣圖資料中，並在32位界限上對齊。 應用程式會讀取 **WIA \_ ipc \_ Thumb \_ 寬度** 和 **WIA \_ ipc \_ Thumb \_ 高度** 屬性的值，並建立 [BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) (在 Platform SDK 檔) 中所述。 應用程式應該能夠讀取 **WIA \_ IPC \_ 縮圖** 屬性 (代表實際的縮圖影像資料) 並使用此屬性直接將這些位寫入新建立的點陣圖，以建立縮圖影像。 這個屬性是由 WIA minidrivers 和在 MicrosoftWindows Me、Windows XP 及更新版本的作業系統上執行的應用程式所使用。<br/> 類型： **vt \_ UI1** \| **vt \_ 向量** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/> |
| <span id="WIA_IPC_THUMB_WIDTH"></span><span id="wia_ipc_thumb_width"></span><dl> <dt>**WIA \_IPC \_ THUMB \_ 寬度**</dt> <dt>CameraPictureThumbWidth</dt> </dl>                         | 包含裝置上所儲存之縮圖影像的目前寬度（以圖元為單位）。 迷你驅動程式會建立並維護此屬性。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="WIA_IPC_THUMB_HEIGHT"></span><span id="wia_ipc_thumb_height"></span><dl> <dt>**WIA \_IPC \_ THUMB \_ 高度**</dt> <dt>CameraPictureThumbHeight</dt> </dl>                     | 包含裝置上所儲存之縮圖影像的目前高度（以圖元為單位）。 迷你驅動程式會建立並維護此屬性。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="WIA_IPC_AUDIO_AVAILABLE"></span><span id="wia_ipc_audio_available"></span><dl> <dt>**WIA \_\_ \_ 可用的 IPC 音訊**</dt> <dt>CameraPictureAudioAvailable</dt> </dl>         | 這個屬性已經過時。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="WIA_IPC_AUDIO_DATA_FORMAT"></span><span id="wia_ipc_audio_data_format"></span><dl> <dt>**WIA \_IPC \_ 音訊 \_ 資料 \_ 格式**</dt> <dt>CameraPictureAudioDataFormat</dt> </dl> | 這個屬性已經過時。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="WIA_IPC_AUDIO_DATA"></span><span id="wia_ipc_audio_data"></span><dl> <dt>**WIA \_IPC \_ 音訊 \_ 資料**</dt> <dt>CameraPictureAudioData</dt> </dl>                             | 這個屬性已經過時。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="WIA_IPC_NUM_PICT_PER_ROW"></span><span id="wia_ipc_num_pict_per_row"></span><dl> <dt>**WIA \_\_ \_ \_ 每個資料 \_ 列 CameraPictureNumPictPerRow 的 IPC NUM PICT**</dt> <dt></dt> </dl>     | 這個屬性保留供日後使用，目前不會執行。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="WIA_IPC_SEQUENCE"></span><span id="wia_ipc_sequence"></span><dl> <dt>**WIA \_IPC \_ 序列**</dt> <dt>CameraPictureSequence</dt> </dl>                                     | 這個屬性保留供日後使用，目前不會執行。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="WIA_IPC_TIMEDELAY"></span><span id="wia_ipc_timedelay"></span><dl> <dt>**WIA \_IPC \_ TIMEDELAY**</dt> <dt>CameraPictureTimedelay</dt> </dl>                                 | 這個屬性保留供日後使用，目前不會執行。<br/> 類型： **VT \_ I4** 的取值：唯讀、有效的值： [WIA 類別 \_ \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 
