---
description: 指出是否 \_ 將接受在輸入範例上設定的 MFSampleExtension ROIRectangle 屬性。
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: 'CODECAPI_AVEncVideoROIEnabled 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86185f6dbb9dfe16a84e7e85c3faddc8da3a7c1ead91dee2b1086e6fafa456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346978"
---
# <a name="codecapi_avencvideoroienabled-property"></a>CODECAPI \_ AVEncVideoROIEnabled 屬性

指出是否將接受在輸入範例上設定的 [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) 屬性。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>備註

預設值為 0。

如果編碼器 MFT 接受非零值，則編碼器應該會接受在輸入範例上設定的 [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




