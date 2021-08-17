---
description: 指定從一組圖片 (GOP) 標頭到下一個 GOP 標頭的圖片數目上限。
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: 'AVEncMPVGOPSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7c82ae5c613bb3e78069be3f39f652d840e19c5d62d095fe020f4186bf975f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119258448"
---
# <a name="avencmpvgopsize-property"></a>AVEncMPVGOPSize 屬性

指定從一組圖片 (GOP) 標頭到下一個 GOP 標頭的圖片數目上限。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPVGOPSize**

## <a name="property-value"></a>屬性值

編碼器可以將此屬性實作為列舉集或線性範圍。

## <a name="remarks"></a>備註

開始錄製之前，請先設定這個屬性。

**適用于 Windows 8：** 編碼的 GOP 大小應透過這個屬性小於或等於指定的數位，以保持在 GOP 中 [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md)所設定的相同 B 框架模式，或因場景變更。 例如，當 GOP 中的 B 框架數目指定為2，而 GOP 大小為11時，則編碼器應產生10個框架以內的 GOP 大小。 當 GOP 中間發生場景變更時，編碼器可能也會插入主要畫面格，並產生較小的 GOP。

GOP 大小0是編碼器相依的，且編碼器可以根據其執行/品質/效能選擇不同的 GOP 大小。 在此情況下，編碼器應接受 GOP 大小並截斷 B 框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




