---
description: 取得型別為 IMFCollection 的物件，其中包含 IMFSample 物件，其中包含網路抽象層單位 (NALUs) 和增補增強資訊 (SEI 由解碼器轉送的) 單位。
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: 'MFSampleExtension_ForwardedDecodeUnits 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2298a29d722c118fb79d5f0b49aa9d3d94fd735150a65772eb15e6da7638445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713728"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>MFSampleExtension \_ ForwardedDecodeUnits 屬性

取得型別為 [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) 的物件，其中包含 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 物件，其中包含網路抽象層單位 (NALUs) 和增補增強資訊 (SEI 由解碼器轉送的) 單位。

## <a name="data-type"></a>資料類型

**IUnknown**

## <a name="remarks"></a>備註

集合包含自先前畫面格起，已移除模擬防止位元組的所有自訂 NALU/SEI 單位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




