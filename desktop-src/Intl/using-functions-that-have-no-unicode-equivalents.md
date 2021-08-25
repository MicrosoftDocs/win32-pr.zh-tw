---
description: 尚未使用 Unicode 版本執行的函式，通常是由支援 Unicode 的功能強大或擴充函數所取代。
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: 使用沒有 Unicode 對應項的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00781db9bce98c335c4a9071b9643ef5fdcb3716478cbffe12a5b53b33e2313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787878"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>使用沒有 Unicode 對應項的函式

尚未使用 [unicode](unicode.md) 版本執行的函式，通常是由支援 unicode 的功能強大或擴充函數所取代。 例如，如果您正在移植呼叫 [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) 函式的程式碼，則您的應用程式可以改為使用 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數來支援 Unicode。

如果函式沒有 Unicode 對等專案，應用程式可以在函式呼叫之前和之後，將字元對應到8位字元集。 例如，數位格式函式 **atoi** 和 **itoa** 只會使用數位0到9。 一般來說，將 Unicode 對應到8位的字元會造成資料遺失，但藉由讓程式碼類型獨立，並讓運算式成為條件式，可避免這種情形。 下列範例中，針對8位字元所撰寫的語句會與型別相依，而且應該變更為支援 Unicode。


```C++
char str[4] = "137";

int num = atoi(str);
```



您可以依照下列方式重寫這些語句，使其與型別無關。


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



在此範例中，標準 C 程式庫函式 **wcstombs** 會將 Unicode 轉換成 ASCII。 此範例的事實是，即使某些周圍文字無法使用，數位0到9也可以永遠從 Unicode 轉譯成 ASCII。 **Atoi** 函式會在非數位的任何字元上停止。

您的應用程式可以使用 (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) 函式的國家語言支援，來處理包含 Unicode 中某些腳本提供之 [原生數位](digit-shapes.md) 的文字。

> [!Caution]  
> 使用 **wcstombs** 函式不正確，可能會危及應用程式的安全性。 請確定8位字元字串的應用程式緩衝區至少為大小 2 \* (*字元 \_ 長度* + 1) ，其中 *char \_ 長度* 代表 Unicode 字串的長度。 這項限制的原因是，使用 [雙位元組字元集](double-byte-character-sets.md) (dbcs) ，每個 Unicode 字元都可以對應到兩個連續的8位字元。 如果緩衝區未保留整個字串，則結果字串不會以 null 結束，因而產生安全性風險。 如需應用程式安全性的詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 和字元集](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
