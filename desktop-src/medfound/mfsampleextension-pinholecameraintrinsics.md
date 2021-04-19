---
description: 包含此範例的 pinhole 攝影機內建函式。
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: 'MFSampleExtension_PinholeCameraIntrinsics 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987467"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a>MFSampleExtension \_ PinholeCameraIntrinsics 屬性

包含此範例的 pinhole 攝影機內建函式。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

屬性的值是 [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics)。

這個屬性是選擇性的，可支援未校正的相機。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




