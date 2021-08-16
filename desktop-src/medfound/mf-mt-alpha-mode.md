---
description: 指定彩色媒體影片類型的 Alpha 模式是預乘或直接。
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: 'MF_MT_ALPHA_MODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c658cae64c68aa89c49230164707d75369c021767c6aa0b46818516ffa26513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035316"
---
# <a name="mf_mt_alpha_mode-attribute"></a>MF \_ MT \_ ALPHA \_ 模式屬性

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

指定彩色媒體影片類型的 Alpha 模式是預乘或直接。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個值可以轉換成 [**DXGI \_ ALPHA \_ 模式**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) 值。 如果這個屬性不存在，為了回溯相容性，此值 **會 \_ \_ \_ 直接** 適用于支援 Alpha 通道的影片格式（例如 ARGB32），或在不含 ALPHA 色板的影片格式（例如 RGB32） **\_ \_ \_ 略** 過。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                      |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 
