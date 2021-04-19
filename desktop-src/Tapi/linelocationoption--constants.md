---
description: LINELOCATIONOPTION \_ 常數會定義 LINELOCATIONENTRY 結構的 >dwoptions 成員所使用的值，這些值會在 lineGetTranslateCaps 所傳回之 LINETRANSLATECAPS 結構的一部分傳回。
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: 'LINELOCATIONOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978441"
---
# <a name="linelocationoption_-constants"></a>LINELOCATIONOPTION \_ 常數

**\_ LINELOCATIONOPTION** 常數會定義 [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry)結構的 **>dwoptions** 成員所使用的值，這些值會在 [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)所傳回之 [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)結構的一部分傳回。

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



這個位置的預設撥號模式是撥盤式撥號。 如果設定此位， [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) 會在選取這個位置時所傳回之可撥出字串的開頭插入 "P" 撥號修飾詞。 如果未設定此位， **lineTranslateAddress** 會在可撥出字串的開頭插入 "T" 撥號修飾詞。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

不可延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




