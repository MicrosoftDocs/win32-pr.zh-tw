---
title: ADSI 擴充模型中的晚期繫結與 Vtable 存取
description: 雙重介面可讓您在分派介面沒有時，對其所有的函式進行直接 vtable 存取。
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- ADSI 擴充模型 ADSI 中的晚期繫結與 vtable 存取
- ADSI 擴充模型中的延伸 ADSI、晚期繫結和 vtable 存取
- adsi adsi，範例程式碼 Visual Basic，使用 IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eacc2008d3da33cd8d1897eeff2c30301849f9ec306656fc494072c33608c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023356"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>ADSI 擴充模型中的晚期繫結與 Vtable 存取

雙重介面可讓您在分派介面沒有時，對其所有的函式進行直接 vtable 存取。 C/c + + 用戶端可以查詢雙重介面指標，並使用直接 vtable 存取來叫用其函數。 這可提供比使用 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 和 [**Idispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 函數叫用函式更快的存取權。 這在擴充模型中更是如此，因為擴充功能物件中的所有雙重介面都必須先委派其 **GetIDsOfNames** **，並** 將函式重新叫用至匯總工具 (ADSI) first。 然後，匯總工具必須執行額外的內部步驟，以識別哪個擴充物件（可能包含匯總工具本身）支援呼叫的函式，並將呼叫重新導向至適當的物件。

Visual Basic 也會使用 vtable 的直接存取叫用雙重介面函式（如果它有介面的指標，並從類型程式庫存取型別資料）。 以 Visual Basic 撰寫的 ADSI 用戶端可以指定雙重介面的指標，例如 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、明確地，並允許 vtable 存取介面中的函式。


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



由於 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面不支援 vtable 存取，因此不適用此範例。 也就是說，只會透過 [**idispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 和 [**Idispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 函數叫用分派函式。

目前的 VBScript 和 JScript 版本也不支援 vtable 存取。 因此，VBScript 或 JScript 環境中的雙重介面會像分派介面一樣執行。

 

 