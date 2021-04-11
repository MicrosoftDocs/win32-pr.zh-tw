---
description: 代表材質格式的描述。
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureFormatDesc 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935873"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc 結構

代表材質格式的描述。

## <a name="syntax"></a>語法


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a>成員

**dxgiFormat**  
材質的 DXGI 格式。

**dataFormat**  
材質的資料格式。

**blockBytes**  
資料區塊中的位元組數目。

**blockHeight**  
在區塊的 Y 軸) 中，高度 (數位樣本。

**blockWidth**  
區塊 X 軸) 中的樣本 (數目。

**channelX**  
描述 X 通道的屬性。 如需詳細資訊，請參閱 PixEngineChannelDescription 結構。

**channelY**  
描述 Y 通道的屬性。 如需詳細資訊，請參閱 PixEngineChannelDescription 結構。

**channelZ**  
描述 Z 通道的屬性。 如需詳細資訊，請參閱 PixEngineChannelDescription 結構。

**channelW**  
描述 W 通道的屬性。 如需詳細資訊，請參閱 PixEngineChannelDescription 結構。

**swizzle**  
描述套用至範例的 swizzle (通道交換) 。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



