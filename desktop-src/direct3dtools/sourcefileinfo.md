---
description: 表示原始程式碼檔的相關資訊。
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SourceFileInfo 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b6afd5f3b383aff5c6d5168b259b13fe4429ac40d5b19a21c8e2f6a207cecd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119232"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo 結構

表示原始程式碼檔的相關資訊。

## <a name="syntax"></a>語法


```C++
} SourceFileInfo;
```

## <a name="members"></a>成員

**檔案名**  
COM 字串 comtaining 相關原始程式檔的 filepath。

**checksumByteCount**  
總和檢查碼中的位元組數目。 當 checkSumAlgorithm 等於 CHECKSUMALGORITHM：： md5 時，checkSumByteCount 是16。 當 checkSumAlgorithm 等於 CHECKSUMALGORITHM：： sha1 時，checkSumByteCount 為20。

**checkSumAlgorithm**  
指定用來產生檔案總和檢查碼的演算法。 支援的演算法為 MD5 和 SHA1。 如需詳細資訊，請參閱 CHECKSUMALGORITHM 列舉。

**checkSumFirstPart**  
總和檢查碼的前8個位元組部分。

**checkSumSecondPart**  
總和檢查碼的第二個8位元組部分。

**checkSumThirdPart**  
總和檢查碼的第三個8位元組部分。

**checkSumFourthPart**  
總和檢查碼的第四個8位元組部分。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



