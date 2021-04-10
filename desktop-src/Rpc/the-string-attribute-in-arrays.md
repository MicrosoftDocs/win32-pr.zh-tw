---
title: 陣列中的字串屬性
description: 您可以針對一維字元陣列、寬字元陣列和代表文字字串的位元組陣列，使用 \ string \ 屬性。
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092963"
---
# <a name="the-string-attribute-in-arrays"></a>\[ \] 陣列中的字串屬性

您可以 \[ [](/windows/desktop/Midl/string) \] 針對一維字元陣列、寬字元陣列和代表文字字串的位元組陣列，使用 string 屬性。 如果您使用 **\[ 字串 \]** 屬性，用戶端 stub 會使用 C 程式庫函數 **strlen** 或 **wstrlen** 來計算字串中的字元數。 為了避免可能的不一致，MIDL 不讓您在 **\[ \]** \[ [第一個 \_ 是](/windows/desktop/Midl/first-is) \] 、 \[ [last \_ 為](/windows/desktop/Midl/last-is) \] ，而且 \[ [size \_ 是](/windows/desktop/Midl/size-is) \] 屬性時，同時使用字串屬性。

在 C 中使用以 null 終止的字串時，您必須允許在字串結尾使用空格作為 null 字元。 例如，在宣告最多80個字元的字串時，會配置81個字元。 下列範例 IDL 檔案示範如何以 **\[ 字串 \]** 屬性宣告陣列。

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 