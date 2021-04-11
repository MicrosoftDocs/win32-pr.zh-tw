---
description: 停用來源讀取器使用後置處理相機外掛程式。
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: 'MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194860"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>MF \_ 來源 \_ 讀取器 \_ 停用 \_ 相機 \_ 外掛程式屬性

停用 [來源讀取器](source-reader.md)使用後置處理相機外掛程式。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

當來源讀取器與影片捕獲來源搭配使用時，會套用此屬性。 如果此屬性為 **TRUE**，則會防止來源讀取器載入相機可能提供的任何後續處理外掛程式。 否則，來源讀取器預設會載入它們。

這個屬性的預設值為 **FALSE**。 當您建立來源讀取器時，請設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> </dl>

 

 




