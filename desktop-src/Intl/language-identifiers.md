---
description: 語言識別項是國家或地區中語言的標準國際數值縮寫。
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: 語言識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991760"
---
# <a name="language-identifiers"></a>語言識別碼

語言識別項是國家或地區中 [語言](locales-and-languages.md) 的標準國際數值縮寫。 每種語言都有唯一的語言識別項 (資料類型 LANGID) ，它是由主要語言識別項和子語言識別項組成的16位值。 如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](language-identifier-constants-and-strings.md)。

語言識別項是使用 [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) 宏所建立。 下圖顯示語言識別項中的位格式。

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

以下是預先定義的語言識別項：

-   LANG \_ 系統 \_ 預設值。 作業系統的預設語言。
-   LANG \_ 使用者 \_ 預設值。 目前使用者的語言。

您的應用程式可以使用 [多語系消費者介面](multilingual-user-interface.md) 函式來取得目前的語言識別項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[地區設定和語言](locales-and-languages.md)
</dt> <dt>

[語言識別項常數和字串](language-identifier-constants-and-strings.md)
</dt> <dt>

[多語系使用者介面](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



