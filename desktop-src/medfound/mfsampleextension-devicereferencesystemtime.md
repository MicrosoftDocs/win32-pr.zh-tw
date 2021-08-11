---
description: 指定範例上的原始裝置時間戳記。
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: 'MFSampleExtension_DeviceReferenceSystemTime 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0458c1a2b0f5b204483cba0e6f571a2a5ace34b7b39463cc20ded664eecaaa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241133"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>MFSampleExtension \_ DeviceReferenceSystemTime 屬性

指定範例上的原始裝置時間戳記。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

這是媒體範例的裝置參考時間戳記（以100ns 解析）。 根據產生範例的來源而定，此時間戳記不一定會包含查詢效能計數器的實際值 (QPC) 。 媒體管線中的其他元件可能會修改此值。 MFTs 插入至 capture 管線時無法使用這個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




