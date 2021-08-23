---
description: 包含資料流程的 pinhole 攝影機內建函式。
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: 'MFStreamExtension_PinholeCameraIntrinsics 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0a77f7d49770e084dfe258169863a713311be02f1711c6f637c7bfc16b4e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973177"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a>MFStreamExtension \_ PinholeCameraIntrinsics 屬性

包含資料流程的 pinhole 攝影機內建函式。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes)。

## <a name="remarks"></a>備註

屬性的值是 [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




