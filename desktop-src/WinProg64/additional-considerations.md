---
title: 其他考量
description: 移植您的程式碼時，請考慮下列幾點。
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- 移植秘訣 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 199f522bebf0d6d5552aa81d99aab12f77685dea35eb329b9e7d11d46b4f1500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561533"
---
# <a name="additional-considerations"></a>其他考量

移植您的程式碼時，請考慮下列幾點：

- 下列假設已不再有效：

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   不過，64位編譯器會定義 \_ WIN32 以提供回溯相容性。

- 下列假設已不再有效：

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   在此情況下，else 子句可代表 \_ WIN32 或 \_ WIN64。

- 請小心使用資料類型對齊。 **類型 \_ 對齊** 宏會傳回資料類型的對齊需求。 例如： `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 （x86）、8（Intel Itanium 處理器 `TYPE_ALIGNMENT( UCHAR )` = = 1）

    例如，核心程式代碼目前看起來像這樣：

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    可能會變更為：

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    Intel Itanium 系統已停用核心模式對齊例外狀況的自動修正。

- 請小心使用 NOT 作業。 請考慮下列事項：

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    問題是 ~ (b-1) 會產生 "0x0000 0000 xxxx"，而不是 "0xFFFF FFFF xxxx"。 編譯器將不會偵測到此情況。 若要修正此問題，請變更程式碼，如下所示：

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- 請小心執行未簽署和簽署的作業。 請考慮下列事項：

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    結果非預期的大小。 規則是，如果任一運算元未簽署，則結果為未簽署。 在上述範例中，會將轉換成不帶正負號的值（除以 b），並將結果儲存在 c 中。 轉換不需要進行數位操作。

    另舉一個範例，請考慮下列事項：

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    發生此問題的原因是 x 不帶正負號，這會使整個運算式不帶正負號。 除非 y 是負值，否則這會正常運作。 在此情況下，會將 y 轉換成不帶正負號的值、使用32位有效位數評估運算式、調整規模，並將其新增至 pVar1。 32位不帶正負號的負數會變成大型的64位正數，以提供錯誤的結果。 若要修正這個問題，請將 x 宣告為帶正負號的值，或在運算式中明確地將它轉換為 **LONG** 。

- 進行分次大小配置時請小心。 例如：

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    下列程式碼是錯誤的，因為編譯器會以額外4個位元組填補結構，以進行8位元組的對齊：

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    下列程式碼是正確的：

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- 請勿傳遞給函式 `(HANDLE)0xFFFFFFFF` ，例如 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)。 相反地，請使用 **不正確 \_ 控制碼 \_ 值**。
- 列印字串時，請使用適當的格式規範。 使用% p 以十六進位列印指標。 這是列印指標的最佳選擇。 Microsoft Visual C++ 支援% I 來列印多型資料。 Visual C++ 也支援% I64 來列印64位的值。

 

 