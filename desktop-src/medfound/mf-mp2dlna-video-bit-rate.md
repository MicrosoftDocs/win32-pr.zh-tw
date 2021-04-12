---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大視頻位元速率。
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: 'MF_MP2DLNA_VIDEO_BIT_RATE 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191892"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>MF \_ MP2DLNA \_ 影片 \_ 位 \_ 速率屬性

指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大視頻位元速率。

## <a name="data-type"></a>資料類型

**UINT32**

值是編碼影片串流的目標最大位元速率，以每秒位數為單位。 最大值為 9800000 (9.8 Mbps) ，這也是預設值。

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。 開始串流之前，請設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmp2dlna。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




