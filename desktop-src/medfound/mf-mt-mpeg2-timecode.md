---
description: 針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包包含4位元組的時間代碼。
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: 'MF_MT_MPEG2_TIMECODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193627"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>MF \_ MT \_ MPEG2 時間 \_ 碼屬性

針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包包含4位元組的時間代碼。

## <a name="data-type"></a>資料類型

**UINT32**



| 值                                                                                                | 意義                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 未新增任何時間碼。<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 每個傳輸封包的開頭會加上4個位元組的時間代碼。 某些數位電視標準需要此時間代碼。<br/> |



 

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

 

 




