---
description: 定義字串的部分或全部字元屬性、圖像、前進寬度、x 和 y 位置、字元對圖像對應等等。
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: 'SCRIPT_STRING_ANALYSIS (Usp10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9481c641f182015d7a318c21c490f45fcc934e0df1baa52483707628eb4daa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390297"
---
# <a name="script_string_analysis"></a>腳本 \_ 字串 \_ 分析

定義字串的部分或全部字元屬性、圖像、前進寬度、x 和 y 位置、字元對圖像對應等等。


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>備註

這是 [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)動態配置及取出的不透明結構。 所有其他 **ScriptString \*** 函式也都需要此功能。

因為分析可能很大，所以您的應用程式必須在完成字串後立即呼叫 [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 可轉散發套件<br/>          | Internet Explorer 5 或更新版本于 windows Me/98/95<br/>                         |
| 標頭<br/>                   | <dl> <dt>Usp10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Uniscribe 結構](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




