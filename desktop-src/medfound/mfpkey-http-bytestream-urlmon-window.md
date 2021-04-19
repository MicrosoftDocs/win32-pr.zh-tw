---
description: 設定 Microsoft 媒體基礎 HTTP 位元組資料流程的視窗。
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: 'MFPKEY_HTTP_ByteStream_Urlmon_Window 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999507"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>MFPKEY \_ HTTP \_ ByteStream \_ urlmon.dll \_ 視窗屬性

設定 Microsoft 媒體基礎 HTTP 位元組資料流程的視窗。 此視窗會在系結作業期間用來顯示使用者介面中的資訊。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**IUnknown\***

VT \_ 不明

**punkVal**



## <a name="remarks"></a>備註

您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。 若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

這個屬性的值是 **IWindowForBindingUI** 介面的指標。 這個屬性只適用于 [MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon.dll](mfpkey-http-bytestream-enable-urlmon.md) 屬性設為 **VARIANT \_ TRUE** 時。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
