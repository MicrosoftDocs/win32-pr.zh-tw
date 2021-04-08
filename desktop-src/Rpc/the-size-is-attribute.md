---
title: Size_is 屬性
description: '\ 的大小 \_ 為 \ 屬性，與指定陣列配置大小的整數常數、運算式或變數相關聯。'
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842400"
---
# <a name="the-size_is-attribute"></a>\[大小 \_ 為 \] Attribute

\[ [Size \_ 是](/windows/desktop/Midl/size-is) \] 與指定陣列配置大小的整數常數、運算式或變數相關聯的屬性。 請考慮長度由使用者輸入決定的字元陣列：

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> \*標示變數陣列維度之預留位置的星號 () 是選擇性的。

 

伺服器 stub 必須在伺服器上配置對應至該參數之用戶端記憶體的記憶體。 指定大小的變數必須一律至少為 \[ [in](/windows/desktop/Midl/in) \] 參數。 需要 **\[ in \]** 方向屬性，以便在進入伺服器 stub 時定義大小值。 此大小值提供伺服器 stub 配置記憶體所需的資訊。

Size 參數也可以是 \[ in、 [out](/windows/desktop/Midl/out-idl) \] 。 比方說，如果用戶端傳送的陣列不足以容納伺服器需要儲存的資料，這就很有用。 您可以使用 **\[ in、out \]** size 參數將所需的大小傳送回用戶端程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多個指標層級](multiple-levels-of-pointers.md)
</dt> </dl>

 

 