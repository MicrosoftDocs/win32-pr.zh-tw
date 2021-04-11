---
description: 針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包是否包含內容封包標頭。
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: 'MF_MT_MPEG2_CONTENT_PACKET 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850456"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>MF \_ MT \_ MPEG2 \_ 內容封 \_ 包屬性

針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包是否包含內容封包標頭。

## <a name="data-type"></a>資料類型

**UINT32**



| 值                                                                                                | 意義                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 未新增任何內容封包標頭。<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 在 200-1000 毫秒的間隔內，會將14位元組的內容封包標頭新增至傳輸封包的開頭，如同無線電產業和企業的關聯所定義 (ARIB) 標準。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




