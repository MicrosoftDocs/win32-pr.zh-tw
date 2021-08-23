---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器的編碼品質。
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: 'MF_MP2DLNA_ENCODE_QUALITY 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a612dae32aabe4276ece76e7edff1aef431cc5d93f8aeaae0dbc9087620374c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973657"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a>MF \_ MP2DLNA \_ 編碼 \_ 品質屬性

指定數位客廳網路聯盟 (DLNA) 媒體接收器的編碼品質。

## <a name="data-type"></a>資料類型

**UINT32**

範圍：0到18

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

較高的數位表示較佳的編碼品質。 數位越低表示編碼速度較快，但編碼品質較低。 預設值為9。

若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。 開始串流之前，請設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmp2dlna。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




