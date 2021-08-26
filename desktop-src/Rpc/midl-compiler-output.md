---
title: MIDL 編譯器輸出
description: 使用 IDL 和 ACF 檔案作為輸入，MIDL 編譯器最多會產生五個 C 語言的原始檔。
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aea74b77d8e709d8a71d3c84f457d301bb38d8c35bdccaa77e9e3033d08ed70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019688"
---
# <a name="midl-compiler-output"></a>MIDL 編譯器輸出

使用 IDL 和 ACF 檔案作為輸入，MIDL 編譯器最多會產生五個 C 語言的原始檔。 根據預設，MIDL 編譯器會在產生的存根檔案中使用 IDL 檔案的基底檔案名。 當基底檔案名中有六個以上的字元時，某些檔案系統可能不會接受完整的存根名稱。 下表顯示檔案名所使用的慣例。



| 檔案        | 基底檔案名的預設部分 | 範例      |
|-------------|-----------------------------------|--------------|
| IDL 檔案    | ---                               | Abcdefgh .idl |
| 標頭      | .h                                | Abcdef。h     |
| 用戶端存根 | \_c. c                             | Abcdef \_ c。  |
| 伺服器 stub | \_s. c                             | Abcdef \_ s. c  |



 

 

 




