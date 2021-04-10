---
description: 包含資料流程的 pinhole 攝影機內建函式。
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: 'MFStreamExtension_PinholeCameraIntrinsics 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ad848f0b8cc12c2496544d98b4ef17332151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943870"
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
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




