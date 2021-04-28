---
title: COM 中的錯誤碼
description: COM 中的錯誤碼
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103956"
---
# <a name="error-codes-in-com"></a>COM 中的錯誤碼

為了表示成功或失敗，COM 方法和函式會傳回 **HRESULT** 類型的值。 **HRESULT** 是32位的整數。 **HRESULT** 的高序位位表示成功或失敗。 零 (0) 表示成功，1表示失敗。

這會產生下列數值範圍：

-   成功碼：0x0 –0x7FFFFFFF。
-   錯誤碼：0x80000000 –0xFFFFFFFF。

少數的 COM 方法不會傳回 **HRESULT** 值。 例如， [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法會傳回不帶正負號的 long 值。 但是傳回錯誤碼的每個 COM 方法都會傳回 **HRESULT** 值。

若要檢查 COM 方法是否成功，請檢查傳回之 **HRESULT** 的高序位位。 Windows SDK 標頭提供兩種可簡化此作業的宏： [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) 的宏和 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 的宏。 如果 **HRESULT** 是成功碼，**成功** 的宏會傳回 **TRUE** ，如果是錯誤碼，則會傳回 **FALSE** 。 下列範例會檢查 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 是否成功。


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



有時候，測試反向條件會比較方便。 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed)的宏會與 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded)的相反。 它會針對錯誤碼傳回 **TRUE** ，並針對成功代碼傳回 **FALSE** 。


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



稍後在本課程模組中，我們將探討如何結構您的程式碼來處理 COM 錯誤的一些實用建議。  (請參閱 [COM 中的錯誤處理](error-handling-in-com.md)。 ) 

## <a name="next"></a>下一個

[在 COM 中建立物件](creating-an-object-in-com.md)

 

 
