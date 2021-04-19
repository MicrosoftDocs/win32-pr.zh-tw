---
description: 指定長期參考 (LTR) 框架資訊，並且在輸出範例上傳回。
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: 'MFSampleExtension_LongTermReferenceFrameInfo 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992237"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>MFSampleExtension \_ LongTermReferenceFrameInfo 屬性

指定長期參考 (LTR) 框架資訊，並且在輸出範例上傳回。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

**H.264/AVC 編碼器：**

當應用程式控制 LTR 框架（由 [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)指定）時，編碼器應該會在輸出範例上傳回這個屬性。

MFSampleExtension \_ LongTermReferenceFrameInfo 會傳回最多兩個欄位。

第一個欄位（位 \[ 0.. 15 \] ） *LongTermFrameIdx* 與輸出框架相關聯（如果它標示為 LTR 框架）。 如果這個輸出框架是短期參考框架或非參考框架，則第一個值是0xffff。

第二個欄位（位 \[ 16.. 31 \] ）是由 *MaxNumLTRFrames* 多個位所組成的點陣圖，表示用來編碼此輸出框架的 (s) ，從位16開始。 其餘的位應設定為0。 如果這個輸出框架未使用任何 LTR 框架編碼，則第二個值是0。 *MaxNumLTRFrames* 是透過 [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)設定之 LTR 框架的最大數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




