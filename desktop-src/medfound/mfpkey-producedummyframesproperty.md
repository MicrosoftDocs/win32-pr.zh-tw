---
description: 指定編碼器是否會在位流中產生重複框架的虛擬框架專案。
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: 'MFPKEY_PRODUCEDUMMYFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192245"
---
# <a name="mfpkey_producedummyframes-property"></a>MFPKEY \_ PRODUCEDUMMYFRAMES 屬性

指定編碼器是否會在位流中產生重複框架的虛擬框架專案。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCProduceDummyFrames

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ FALSE

## <a name="remarks"></a>備註

如果此值為 VARIANT \_ FALSE，則編解碼器不會將任何資料放在位資料流程中，以供重複的畫面格之用。

在保存框架編號的應用程式中，虛擬框架可能很重要。 常見的範例是針對編碼的內容維護 SMPTE 時間代碼。

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

 

 




