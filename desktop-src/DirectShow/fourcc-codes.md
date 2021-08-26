---
description: FOURCC 碼
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: FOURCC 碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25820d21fb8e8386fb11816c373debf427fa783b8a2f2d4723a46e689e6aea0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043318"
---
# <a name="fourcc-codes"></a>FOURCC 碼

許多數位媒體格式都有指派的 FOURCC 碼。 FOURCC 程式碼是串連四個 ASCII 字元所建立的32位不帶正負號的整數。 例如，YUY2 video 的 FOURCC 程式碼為 ' YUY2 '。 針對壓縮的影片格式和非 RGB 影片格式 (例如 YUV) ， [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的 **biCompression** 成員應設定為 FOURCC 程式碼。

有各種 C/c + + 宏，可讓您更輕鬆地在原始程式碼中宣告 FOURCC 值。 例如， **MAKEFOURCC** 宏是在 Mmsystem 中宣告，而 **FCC** 宏則是在 Aviriff 中宣告。 使用方式如下：


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



您也可以藉由反轉字元順序，直接將 FOURCC 程式碼宣告為字串常值。 例如：


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



必須反轉順序是必要的，因為 Microsoft Windows 作業系統使用的是位元組由大到小的架構。 ' Y ' = 0x59，' U ' = 0x55，' 2 ' = 0x32，因此 ' 2YUY ' 為0x32595559。

### <a name="converting-fourcc-codes-to-subtype-guids"></a>將 FOURCC 碼轉換成子類型 Guid

2 \* 32 guid 的範圍是保留來代表 FOURCCs。 這些 Guid 全都是 `XXXXXXXX-0000-0010-8000-00AA00389B71` `XXXXXXXX` FOURCC 程式碼的形式。 因此，YUY2 的子類型 GUID 為 `32595559-0000-0010-8000-00AA00389B71` 。

其中有許多 Guid 已定義在標頭檔 Uuid 中。 例如，YUY2 子類型定義為 MEDIASUBTYPE \_ YUY2。 DirectShow 基類程式庫也會提供 helper 類別 [**FOURCCMap**](fourccmap.md)，可用來將 FOURCC 碼轉換成 GUID 值。 **FOURCCMap** 函式會採用 FOURCC 程式碼作為輸入參數。 然後，您可以將 **FOURCCMap** 物件轉換成對應的 GUID：


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**音訊子類型**](audio-subtypes.md)
</dt> <dt>

[影片子類型](video-subtypes.md)
</dt> <dt>

[使用編解碼器](working-with-codecs.md)
</dt> </dl>

 

 



