---
description: 下表所列的函式會將字元字串從某個字串類型轉譯成另一個字串類型。
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: 字串類型之間的轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974298"
---
# <a name="translation-between-string-types"></a>字串類型之間的轉譯

下表所列的函式會將字元字串從某個字串類型轉譯成另一個字串類型。



| 函式                                           | 描述                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | 將一個字元字串轉譯為另一個字元字串。             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | 依地區設定對應字元字串。                      |
| [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | 將虛擬按鍵程式碼轉譯為 Unicode 字元。 |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | 將多位元組字元串對應至 Unicode 字串。            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | 將 Unicode 字串對應到多位元組字元串。            |



 

[**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)和 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)函數特別適用于支援數個字串類型的應用程式。 ANSI C 也定義了 **wcstombs** 和 **mbstowcs** 的轉換函式，但是只能在標準 C 程式庫所支援的字元集之間進行轉換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows API 中的 Unicode](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
