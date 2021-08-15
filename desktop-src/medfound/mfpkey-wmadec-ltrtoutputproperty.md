---
description: 指定解碼器是否應該執行 Lt-Rt 折迭。
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: 'MFPKEY_WMADEC_LTRTOUTPUT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76d086fd0f57262d249784fcabc5a98e8a18668cf0697618f3fbbe5528a2cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713808"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>MFPKEY \_ WMADEC \_ LTRTOUTPUT 屬性

指定解碼器是否應該執行 Lt-Rt 折迭。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

如果這個屬性的值為 VARIANT \_ FALSE，且輸出為身歷聲，則音訊解碼器會使用簡單的通道折迭。 如果這個屬性的值為 VARIANT \_ TRUE，音訊解碼器會執行 Lt-Rt (matrixed) 折迭到身歷聲，然後使用任何杜住的範圍解碼器來解碼 matrixed 環繞。 例如，音訊解碼器可能會在5.1 或7.1 內容上執行 Lt-Rt 折迭。

只有當解碼器作為 DirectX 媒體物件 (DMO) 時，才支援此屬性。 當解碼器作為媒體基礎轉換 (MFT) 時，不支援任何種類的折迭。

在 Windows Vista 中，如果您在音訊解碼器上取得 **IPropertyStore** 介面，則該解碼器會作為 MFT。 因此，此屬性無法在 Windows Vista 上使用。 如需何時將解碼器作為 DMO 或 MFT 的詳細資訊，請參閱[編解碼器物件](codecobjects.md)底下的個別編解碼器參考頁面。

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

 

 
