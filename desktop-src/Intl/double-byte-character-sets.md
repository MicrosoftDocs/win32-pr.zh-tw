---
description: 雙位元組字集 (DBCS) ，也稱為 &\# 0034; 展開的8位字元集&\# 0034;，是實作為字碼頁的擴充單一位元組字元集 (SBCS) 。
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: 雙位元組字集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbef827b91c5ed2468b06f759883c0ba0b874e74038871227aabe0f65f1a046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147661"
---
# <a name="double-byte-character-sets"></a>雙位元組字集

雙位元組字元集 (DBCS) （也稱為「擴充的8位字元集」）是一組擴充的 [單一位元組字元集](single-byte-character-sets.md) (SBCS) ，會實作為字碼頁。 Dbcs 最初是為了擴充 SBCS 設計來處理日文和中文等語言而開發的。 DBCS 中的某些字元（包括用來撰寫英文的數位和字母）具有單一位元組的程式碼值。 其他字元（例如中文表意文字或日文漢字）有雙位元組代碼值。 DBCS 可對應至 Windows 字碼頁或 OEM 字碼頁。 DBCS 字碼頁也可以包含非原生字碼頁，例如，EBCDIC 字碼頁。 如需這些字碼頁的定義，請參閱 [字碼頁](code-pages.md)。

> [!Note]  
> 新的 Windows 應用程式應該使用[Unicode](unicode.md) ，以避免不同的程式字碼頁不一致，並方便當地語系化。 不過，某些舊版通訊協定可能需要使用 DBCS 字碼頁。 每個 DBCS 字碼頁支援不同的字元，但沒有任何頁面支援 Unicode 提供的完整字元範圍。 每個 DBCS 字碼頁支援不同的子集，以不同方式編碼。 從某個 DBCS 字碼頁轉換成另一個的資料會受到損毀，因為不同字碼頁上的相同資料值可以編碼不同的字元。 從 Unicode 轉換為 DBCS 的資料會受到資料遺失的影響，因為指定的字碼頁可能無法表示該特定 Unicode 資料中使用的每個字元。

 

若要解讀 DBCS 字串，應用程式必須從字串的開頭開始並向前掃描。 它會追蹤其在字串中遇到前導位元組的時間，並將下一個位元組視為相同字元的尾端部分。 如果應用程式一次只掃描一個位元組的字串，並遇到表示反斜線 ( "" ) 的位元組，則 \\ 該位元組可能只是兩個位元組字元的後隨位元組。 應用程式不能只備份一個位元組來查看上述位元組是否為前導位元組，因為該位元組值可能有資格同時當做前導位元組和後隨位元組使用。 因此，應用程式基本上與可能的反斜線有相同的問題。 換句話說，使用 DBCS 比 SBCSs 或 Unicode 更複雜的子字串搜尋。 因此，支援 DBCS 的應用程式必須使用特殊的函式，例如 [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l)，而不是 [**StrStr**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx)函數。

您的應用程式會使用 DBCS Windows 字碼頁搭配 "A" 版本的 Windows 函式。 請參閱函數原型和[字碼頁](code-pages.md)[的慣例](conventions-for-function-prototypes.md)。 為了協助識別 DBCS 字碼頁，應用程式可以使用 [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) 或 [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) 函數。 應用程式可以使用 [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) 函式來判斷指定的值是否可以當做2位元組字元的前導位元組使用。 此外，應用程式可以使用 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 函式，在 Unicode 和 DBCS 字串之間進行對應。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字元集](character-sets.md)
</dt> <dt>

[單一位元組字元集](single-byte-character-sets.md)
</dt> </dl>

 

 
