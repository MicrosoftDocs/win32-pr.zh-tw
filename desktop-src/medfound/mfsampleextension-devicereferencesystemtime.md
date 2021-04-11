---
description: 指定範例上的原始裝置時間戳記。
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: 'MFSampleExtension_DeviceReferenceSystemTime 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848445"
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
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




