---
description: 停用在 capture 引擎中 (MFTs) 的硬體媒體基礎轉換。
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: 'MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983545"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>MF \_ 捕獲 \_ 引擎 \_ 停用 \_ 硬體 \_ 轉換屬性

停用在 capture 引擎中 (MFTs) 的硬體媒體基礎轉換。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

根據預設，「捕獲引擎」會使用硬體解碼器或編碼器。 若要停用硬體 MFTs，請在建立 capture 引擎時將此屬性設定為 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




