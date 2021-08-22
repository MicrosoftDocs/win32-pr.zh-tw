---
description: 指定編碼器支援的最大 QP。
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: 'CODECAPI_AVEncVideoMaxQP 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d95f605dbb647ed96ec40e89870c761400a6d414cd354cb0197bb316bd3cf27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606318"
---
# <a name="codecapi_avencvideomaxqp-property"></a>CODECAPI \_ AVEncVideoMaxQP 屬性

指定編碼器支援的最大 QP。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoMaxQP**

## <a name="remarks"></a>備註

**H.264/AVC 編碼器：**

編碼器應支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。

這是靜態屬性，表示只能在編碼會話開始之前設定。

預設值必須是相對應的編碼標準所允許的最大 QP。 例如，h.264 編碼器的預設值應為51。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

