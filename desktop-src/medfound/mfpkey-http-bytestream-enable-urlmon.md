---
description: 啟用 Microsoft 媒體基礎的 HTTP 位元組資料流程，以使用 URL 名字 (也稱為) 。
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: 'MFPKEY_HTTP_ByteStream_Enable_Urlmon 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ede2b9109a7345f3a0d764f6a8fa68952686c5ca05207d01bb0a2e54cea4d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344378"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ urlmon.dll 屬性

啟用 Microsoft 媒體基礎的 HTTP 位元組資料流程，以使用 URL 名字 (也 *稱為)* 。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>備註

您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。 若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

如果值為 **VARIANT \_ TRUE**，HTTP 位元組資料流程會使用 Http 傳輸的 urlmon.dll。 否則，如果值為 **VARIANT \_ FALSE**，則位元組資料流程會使用 WinHTTP。

Windows Store 應用程式的預設值為 **variant \_ TRUE** ，Windows desktop 應用程式的預設值為 variant **\_ FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
