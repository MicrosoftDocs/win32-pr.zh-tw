---
description: 指定在將目前的框架編碼之前，編解碼器將評估之目前畫面格的框架數目。
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: 'MFPKEY_LOOKAHEAD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa5b11abbacc19a4a66dda785d628b1f5d67f636a0f02c7392402ad64a7c3926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113328"
---
# <a name="mfpkey_lookahead-property"></a>MFPKEY \_ 先行屬性

指定在將目前的框架編碼之前，編解碼器將評估之目前畫面格的框架數目。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCLookAhead

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

當編解碼器使用先行完成時，它可以更有效率地編碼影片。

Windows 媒體格式 SDK 的寫入器物件預期編解碼器可以立即編碼每個範例。 如此一來，這項功能在使用寫入器物件的軟體中無法正常運作 (包括 Windows 媒體編碼器和 Windows Media Player) 。 與影片框架相關聯的任何資料單位延伸模組都會附加至錯誤的輸出框架。 資料單位擴充功能放在其中的框架數目，等於所使用的向前擴展框架數目。

有效的右值範圍從0到16個框架。 建議值為16。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




