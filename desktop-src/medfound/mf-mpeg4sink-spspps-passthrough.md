---
description: 指定是否將 MPEG-2 檔案接收篩選出 sequence 參數集 (SPS) 和圖片參數集 (PPS) NALUs。
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: 'MF_MPEG4SINK_SPSPPS_PASSTHROUGH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691815"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>MF \_ MPEG4SINK \_ SPSPPS \_ 傳遞屬性

指定是否將 [**mpeg-2 檔案接收**](mpeg-4-file-sink.md) 篩選出 sequence 參數集 (SPS) 和圖片參數集 (PPS) NALUs。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="applies-to"></a>適用於

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>備註

[**Mpeg-2 檔案接收**](mpeg-4-file-sink.md)會將 SP 和 PPS 參數寫入至「數量」檔案的 [範例描述] 方塊中。 根據預設，它會從影片串流篩選出 SPS 和 PPS NALUs。 若要覆寫此行為，請將 [MF \_ MPEG4SINK \_ SPSPPS \_ 傳遞] 屬性設定為 [ **TRUE**]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




