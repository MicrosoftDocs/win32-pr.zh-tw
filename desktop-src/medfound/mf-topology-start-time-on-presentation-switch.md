---
description: 指定在第一個簡報之後排入的簡報開始時間。
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: 'MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978819"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>\_ \_ \_ \_ \_ PRESENTATION \_ SWITCH 屬性的 MF 拓撲開始時間

指定在第一個簡報之後排入的簡報開始時間。

## <a name="data-type"></a>資料類型

**INT64** 儲存為 **UINT64**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。

## <a name="applies-to"></a>套用至

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

當應用程式將媒體會話上的第一個簡報排入佇列時，應用程式會在 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)方法的 *pvarStartPosition* 參數中指定開始時間。 不過，在任何後續的簡報中，開始時間是由 \_ \_ 拓撲上的 [ \_ \_ \_ PRESENTATION SWITCH] \_ 屬性的 [MF 拓撲開始時間] 所指定。 開始時間是以 100-毫微秒單位（相對於簡報開頭）來指定。 例如，如果值為50000000，播放會在簡報中開始5秒。 如果未設定此屬性，則預設開始時間為零。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




