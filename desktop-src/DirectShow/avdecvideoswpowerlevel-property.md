---
description: 指定視頻解碼器的省電層級。
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: 'AVDecVideoSWPowerLevel 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c362e066a16e333cda402704a720b5e1b0b8534f1b56536d32009e6fa29663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824218"
---
# <a name="avdecvideoswpowerlevel-property"></a>AVDecVideoSWPowerLevel 屬性

指定視頻解碼器的省電層級。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>屬性值

可能值的範圍為 \[ 0 和 100 \] （含），具有下列意義。



| 值 | 描述                 |
|-------|-----------------------------|
| 0     | 針對電池壽命進行優化。  |
| 100   | 針對影片品質進行優化。 |



 

[**EAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)列舉會定義此範圍內的某些特定常數。

## <a name="remarks"></a>備註

您可以在播放期間設定此屬性，以變更省電層級。

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

 

 




