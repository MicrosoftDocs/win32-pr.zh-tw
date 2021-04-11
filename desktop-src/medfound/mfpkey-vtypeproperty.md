---
description: 指定編解碼器將用來偵測交錯式來源影片的邏輯。
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: 'MFPKEY_VTYPE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848452"
---
# <a name="mfpkey_vtype-property"></a>MFPKEY \_ VTYPE 屬性

指定編解碼器將用來偵測交錯式來源影片的邏輯。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCVType

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個屬性可以設定為下列其中一個值。



| 值 | 描述                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 編解碼器將會使用標準的框架類型偵測邏輯。                                                                                 |
| 1     | 編解碼器會將所有來源影片框架視為交錯框架。                                                                          |
| 2     | 編解碼器會將所有來源影片框架視為交錯式影片的欄位。                                                                 |
| 3     | 編解碼器會自動判斷輸入的影片畫面是交錯的框架或交錯式影片的欄位。                      |
| 4     | 編解碼器會自動判斷輸入的影片畫面是漸進式的框架、交錯的框架或交錯式影片的欄位。 |



 

這個屬性會決定漸進式或交錯式影片編碼所使用的圖片編碼方法。

如果未指定任何影片類型，編解碼器將會使用漸進式編碼會話的漸進式幀編碼，以及交錯編碼會話的欄位交錯編碼。 影片編碼會話的類型 (漸進式或交錯式) 是使用 [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) 屬性來設定。

> [!Note]  
> [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md)屬性必須設定為 VARIANT \_ TRUE，才能產生交錯輸出; 否則，設定 MPFKEY \_ VTYPE 屬性將沒有任何作用。

 

當交錯式影片經過編碼時，可以指定數個圖片編碼方法。 編碼交錯式影片的最有效率方式通常是使用 (2) 的「欄位交錯」方法。 如果來源影片包含很少的動作，框架交錯方法 (1) 或自動框架/欄位方法 (2) 可能更適合。

編碼混合的內容 (同時包含漸進式和交錯的框架) 時，最好使用 value auto frame/field/累進方法 (4) 。

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

 

 




