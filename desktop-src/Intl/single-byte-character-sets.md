---
description: 單一位元組字元集 (SBCS) 是將256個個別字符對應到它們的識別程式碼值（實作為字碼頁）。
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: 單一位元組字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bb0150dfaf2e3b8e8251530fd5e90e7b1ede3b3597d344e5efb192fa96ed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130228"
---
# <a name="single-byte-character-sets"></a>單一位元組字元集

單一位元組字元集 (SBCS) 是將256個個別字符對應到它們的識別程式碼值（實作為字碼頁）。 SBCS 可對應至 Windows 字碼頁或 OEM 字碼頁。 SBCS 字碼頁也可以包含非原生字碼頁，例如，EBCDIC 字碼頁。 如需這些字碼頁的定義，請參閱 [字碼頁](code-pages.md)。

> [!Note]  
> 新的 Windows 應用程式應該使用[Unicode](unicode.md) ，以避免不同的程式字碼頁不一致，並方便當地語系化。 不過，某些舊版通訊協定需要使用 SBCS。 每個 SBCS 字碼頁支援不同的字元，但沒有任何頁面支援 Unicode 提供的完整字元範圍。 每個 SBCS 字碼頁支援不同的子集，並以不同方式編碼。 從一個 SBCS 字碼頁轉換成另一個字碼頁的資料可能會損毀，因為不同字碼頁上的相同資料值可以編碼不同的字元。 從 Unicode 轉換成 SBCS 的資料會受到資料遺失的影響，因為指定的字碼頁可能無法表示該特定 Unicode 資料中使用的每個字元。

 

您的應用程式會使用 SBCS Windows 字碼頁搭配 "A" 版本的 Windows 函式。 請參閱函數原型和[字碼頁](code-pages.md)[的慣例](conventions-for-function-prototypes.md)。 為了協助識別 SBCS 字碼頁，應用程式可以使用 [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) 或 [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) 函數。 此外，應用程式可以使用 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 函式，在 Unicode 和 SBCS 字串之間進行對應。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字元集](character-sets.md)
</dt> <dt>

[雙位元組字集](double-byte-character-sets.md)
</dt> </dl>

 

 



