---
description: 管理字元的 Windows API 函式通常會以下列三種格式的其中一種來執行：
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Windows API 中的 Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979921"
---
# <a name="unicode-in-the-windows-api"></a>Windows API 中的 Unicode

管理字元的 Windows API 函式通常會以下列三種格式的其中一種來執行：

-   可以針對 Windows 字碼頁或 Unicode 編譯的泛型版本
-   具有字母 "A" 的 [Windows 字碼頁](code-pages.md) 版本，用來表示 "ANSI"
-   [Unicode](unicode.md)版本，其字母 "W" 用來表示「寬」

某些較新的函式只支援 Unicode 版本。 如需詳細資訊，請參閱 [函數原型的慣例](conventions-for-function-prototypes.md)。

下列主題討論 Unicode 資料類型，以及它們在函式和訊息中的使用方式;使用資源、檔案名和命令列引數;以及在不同類型的字串之間轉譯的方法。

-   [自動訊息轉譯](automatic-message-translation.md)
-   [檔案名中使用的字元集](character-sets-used-in-file-names.md)
-   [命令列引數](command-line-arguments.md)
-   [函數原型的慣例](conventions-for-function-prototypes.md)
-   [標準 C 函數](standard-c-functions.md)
-   [字串函數差異](string-function-differences.md)
-   [字串類型之間的轉譯](translation-between-string-types.md)
-   [字串的 Windows 資料類型](windows-data-types-for-strings.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Unicode 和字元集](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



