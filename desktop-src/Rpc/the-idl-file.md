---
title: IDL 檔案
description: IDL 檔案包含一或多個介面定義，其中每個都有標頭和主體。
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f46a92fe5967dca1faeca1d658cf398fb0baf6ebd9160c3a736747de324e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924412"
---
# <a name="the-idl-file"></a>IDL 檔案

IDL 檔案包含一或多個介面定義，其中每個都有標頭和主體。 標頭包含適用于整個介面的資訊，例如 UUID。 這項資訊會以方括弧括住，後面接著關鍵字 **介面** 和介面名稱。 本文包含 C 樣式的資料類型定義和函式原型，並以描述如何透過網路傳輸資料的屬性來擴充。

在此範例中，介面標頭只包含 UUID 和版本號碼。 版本號碼可確保在有多個版本的 RPC 介面時，只會連接相容的用戶端和伺服器版本。

介面主體包含 **HelloProc** 的函式原型。 在此原型中，函數參數 pszString 具有 **\[** [](/windows/desktop/Midl/in) **\]** 和 **\[** [**字串**](/windows/desktop/Midl/string)中的屬性 **\]** 。 **\[ In \]** 屬性會告知執行時間程式庫，參數只會從用戶端傳遞至伺服器。 **\[ 字串 \]** 屬性會指定存根應將參數視為 C 樣式字元字串。

用戶端應用程式應該能夠關閉伺服器應用程式，因此介面會包含另一個遠端函式 **關閉** 的原型，稍後在本教學課程中將會執行此程式。

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 