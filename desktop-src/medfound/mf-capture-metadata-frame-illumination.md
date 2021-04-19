---
description: 值，指出框架是否使用主動紅外線 (IR) 照明來捕捉。
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: 'MF_CAPTURE_METADATA_FRAME_ILLUMINATION 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974129"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>MF \_ 捕獲 \_ 中繼資料 \_ 框架 \_ 照明屬性

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

值，指出框架是否使用主動紅外線 (IR) 照明來捕捉。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

這個屬性是位元遮罩。 它是64位的值，可提供回溯相容性。

作用中的照明是當裝置有接近 IR 攝影機的燈光發射器發出燈光來照亮場景時，通常會發出 IR 燈，因此不會干擾人類眼睛。 將值設定為 (值 & 0x1) ！ = 0 如果在使用中的照明時捕捉到框架，並將 (值設定為 & 0x1) = = 0 （如果作用中的照明已關閉）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                      |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




