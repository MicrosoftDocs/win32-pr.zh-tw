---
description: 啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的說話者填滿。
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: 'AVDSPSpeakerFill 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff4886f1b6f1e6ae19f9f1b5bf78e20159df390f2d642ac2b9cb3c4c834d1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663429"
---
# <a name="avdspspeakerfill-property"></a>AVDSPSpeakerFill 屬性

啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的說話者填滿。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDSPSpeakerFill**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill) 列舉的成員。

## <a name="remarks"></a>備註

說話者填滿是將 mono 或身歷聲音訊轉換成多頻道音訊的 DSP 流程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




