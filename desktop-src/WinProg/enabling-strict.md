---
title: 啟用 STRICT
description: 當您定義 STRICT 符號時，會啟用在宣告和使用類型時需要更多注意的功能。
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "106974744"
---
# <a name="enabling-strict"></a>啟用 STRICT

當您定義 **STRICT** 符號時，會啟用在宣告和使用類型時需要更多注意的功能。 這可協助您撰寫更多可移植的程式碼。 這種額外的小心也會減少您的調試時間。 啟用 **STRICT** 會重新定義某些資料類型，讓編譯器不允許在沒有明確轉換的情況下，從某個類型指派給另一個類型。 這對 Windows 程式碼特別有用。 傳遞資料類型的錯誤會在編譯時期報告，而不會在執行時間造成嚴重錯誤。

使用 Visual C++，預設會定義 **嚴格** 的類型檢查。

若要定義逐檔案的 **STRICT** ，請在包含 Windows .h 之前插入 **\# define** 語句：


```C++
#define STRICT
#include <windows.h>
```



當定義 **STRICT** 時， [資料類型](windows-data-types.md) 定義會變更，如下所示：

-   特定的控制碼類型已定義為互斥;例如，您將無法在需要 **HDC** 型別引數的情況下傳遞 **HWND** 。 如果沒有 **STRICT**，所有控制碼都會定義為 **控制碼**，因此編譯器不會防止您使用某種類型的控制碼，也就是預期的另一種類型。
-   所有的回呼函數類型 (例如對話方塊程式、視窗程式和攔截程式) 都會以完整原型定義。 這可防止您以不正確的參數清單宣告回呼函數。
-   應使用泛型指標的參數和傳回值型別，會正確宣告為 **LPVOID** ，而不是 **LPSTR** 或其他指標類型。
-   [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat)結構是根據 ANSI 標準來宣告。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[停用 STRICT](disabling-strict.md)
</dt> <dt>

[嚴格合規性](strict-compliance.md)
</dt> </dl>

 

 
