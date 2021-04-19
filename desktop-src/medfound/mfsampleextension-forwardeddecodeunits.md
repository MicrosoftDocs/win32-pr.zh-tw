---
description: 取得型別為 IMFCollection 的物件，其中包含 IMFSample 物件，其中包含網路抽象層單位 (NALUs) 和增補增強資訊 (SEI 由解碼器轉送的) 單位。
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: 'MFSampleExtension_ForwardedDecodeUnits 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971732"
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
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




