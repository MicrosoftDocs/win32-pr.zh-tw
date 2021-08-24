---
description: '&\# 0034; 字元集&\# 0034; 是字元與其識別程式碼值的對應。'
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: 字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f9bb57dad6924e2bbc9390d7315dbed0c59647cacefb932d7055ea8fdd3385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898798"
---
# <a name="character-sets"></a>字元集

「字元集」是字元與其識別程式碼值的對應。 現今電腦最常使用的字元集是 [Unicode](unicode.md)，也是字元編碼的通用標準。 Windows 的應用程式會在內部使用 utf-16 的 Unicode 實作為。 在 UTF-16 中，大部分的字元都是由兩個位元組的代碼所識別。 較不常用的補充字元分別是由一組成對的雙位元組代碼來表示。 如需詳細資訊，請參閱 [代理程式和補充字元](surrogates-and-supplementary-characters.md)。

某些 Windows 的應用程式必須使用 Windows Me/98/95 原生的舊版字元集。 [Windows 字碼頁](code-pages.md)可讓您的應用程式使用這些字元集。 這些字元集可以分為：

-   [單一位元組字元集](single-byte-character-sets.md) (SBCS) 。 在 SBCS 中，每個字元都是以一個位元組寬的值來識別。
-   多位元組字元集，特別是 [雙位元組](double-byte-character-sets.md) 字集 (DBCS) 。 多位元組字元集提供表示許多亞洲語言的大量字元。

如需詳細資訊，請參閱下列主題：

-   [字碼頁](code-pages.md)
-   [雙位元組字集](double-byte-character-sets.md)
-   [單一位元組字元集](single-byte-character-sets.md)
-   [代理和補充字元](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Unicode 和字元集](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



