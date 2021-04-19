---
description: 提供從 base64 產生亂數、轉換及編碼和解碼的功能。
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: 公用程式物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979520"
---
# <a name="utilities-object"></a>公用程式物件

\[**公用程式** 物件可在 [需求] 區段中指定的作業系統中使用。\]

**公用程式** 物件提供從 base64 產生亂數、轉換及編碼和解碼的功能。

## <a name="when-to-use"></a>使用時機

**公用程式** 物件是用來執行下列工作：

-   以 base64 編碼字串，或從 base64 解碼字串。
-   將二進位壓縮的字串轉換成位元組陣列，反之亦然。
-   將二進位壓縮的字串轉換成十六進位字串，反之亦然。
-   產生安全的亂數字。
-   將當地時間轉換為國際標準時間 (格林威治標準時間) ，反之亦然。

## <a name="members"></a>成員

**公用程式** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**公用程式** 物件有這些方法。



| 方法                                                               | 描述                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Base64Decode**](utilities-base64decode.md)                       | 從 base64 解碼字串。<br/>                                     |
| [**Base64Encode**](utilities-base64encode.md)                       | 以 base64 編碼字串。<br/>                                       |
| [**BinaryStringToByteArray**](utilities-binarystringtobytearray.md) | 將二進位壓縮的字串轉換成位元組陣列。<br/>             |
| [**BinaryToHex**](utilities-binarytohex.md)                         | 將二進位壓縮的字串轉換成十六進位字串。<br/>          |
| [**ByteArrayToBinaryString**](utilities-bytearraytobinarystring.md) | 將位元組陣列轉換為二進位壓縮的字串。<br/>             |
| [**GetRandom**](utilities-getrandom.md)                             | 產生安全的亂數字。<br/>                                 |
| [**HexToBinary**](utilities-hextobinary.md)                         | 將十六進位字串轉換為二進位壓縮的字串。<br/>          |
| [**LocalTimeToUTCTime**](utilities-localtimetoutctime.md)           | 將電腦的當地時間轉換成國際標準時間。<br/> |
| [**UTCTimeToLocalTime**](utilities-utctimetolocaltime.md)           | 將國際標準時間轉換為電腦的本地時間。<br/> |



 

## <a name="remarks"></a>備註

您可以建立 **公用程式** 物件，而且可以安全地進行腳本處理。 **公用程式** 物件的 PROGID 為 CAPICOM。公用事業。1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




