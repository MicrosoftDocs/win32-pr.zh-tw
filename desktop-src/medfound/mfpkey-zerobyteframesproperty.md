---
description: 指定要略過的影片畫面格數目，因為它們與先前的畫面格重複。
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: 'MFPKEY_ZEROBYTEFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848448"
---
# <a name="mfpkey_zerobyteframes-property"></a>MFPKEY \_ ZEROBYTEFRAMES 屬性

指定要略過的影片畫面格數目，因為它們與先前的畫面格重複。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCZeroByteFrames

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

在計算編碼的畫面格數目 ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)) 時，不會從傳遞的框架總數 ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) 減去此值。

您可以將 [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) 設定為 VARIANT TRUE，以防止編解碼器略過重複的畫面格 \_ 。

完成傳遞範例之後，您可以取得此值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




