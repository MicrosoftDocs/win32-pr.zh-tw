---
description: 指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: 'MFPKEY_KEYDIST 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848808"
---
# <a name="mfpkey_keydist-property"></a>MFPKEY \_ KEYDIST 屬性

指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCKeyframeDistance

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

預設值取決於正在執行的 Windows 版本，如下表所示。



| 作業系統 | 預設值 |
|------------------|---------------|
| Windows XP       | 8000          |
| Windows Vista    | 8000          |
| Windows 7        | 2000          |



 

## <a name="remarks"></a>備註

編解碼器的內部邏輯會決定每個主要畫面格的實際位置。 任何兩個主要畫面格之間的距離可能小於這個屬性的值，不過，它永遠不會大於。

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

 

 




