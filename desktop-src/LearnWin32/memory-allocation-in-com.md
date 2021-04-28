---
title: COM 中的記憶體配置
description: COM 中的記憶體配置
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103886"
---
# <a name="memory-allocation-in-com"></a>COM 中的記憶體配置

有時候，方法會在堆積上配置記憶體緩衝區，並將緩衝區的位址傳回給呼叫端。 COM 會定義一組函數來配置和釋放堆積上的記憶體。

-   [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)函數會配置記憶體區塊。
-   [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)函式會釋放以 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)配置的記憶體區塊。

在 [ [開啟] 對話方塊範例](example--the-open-dialog-box.md)中，我們看到這個模式的範例：


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



[**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)方法會配置字串的記憶體。 方法會在內部呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置字串。 當方法傳回時， *pszFilePath* 會指向新緩衝區的記憶體位置。 呼叫端會負責呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放記憶體。

為什麼 COM 會定義自己的記憶體配置函數？ 其中一個原因是要在堆積配置器上提供抽象層。 否則，某些方法可能會呼叫 **malloc** ，而其他方法則稱為 **new**。 然後，在某些情況下，您的程式需要 **免費** 通話，並在其他情況下 **刪除** ，並持續追蹤所有的情況。 COM 配置函數會建立一致的方法。

另一個考慮是 COM 是 *二進位* 標準，因此不會系結至特定的程式設計語言。 因此，COM 無法依賴任何特定語言的記憶體配置形式。

## <a name="next"></a>下一個

[COM 編碼作法](com-coding-practices.md)

 

 
