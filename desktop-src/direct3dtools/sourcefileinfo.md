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
ms.openlocfilehash: 39fdb9e7236dea1c04eb55614d9ea9833f398a94
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623124"
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



