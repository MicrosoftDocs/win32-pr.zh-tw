---
title: DllSurrogateExecutable
description: 讓 DLL 伺服器能夠在自訂的代理程式中執行，並與 DllSurrogate 登錄值搭配使用。 如果未指定 DllSurrogateExecutable，COM 會將 Null 傳遞為 CreateProcess 函數的第一個參數值。
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- DllSurrogateExecutable 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fc12af22d1f85c2d2e5ff6e75b2904c5fc5eea636a64e314f997ff36a44e38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373378"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

讓 DLL 伺服器能夠在自訂的代理程式中執行，並與 [**DllSurrogate**](dllsurrogate.md) 登錄值搭配使用。 如果未指定 **DllSurrogateExecutable** ，COM 會將 **Null** 傳遞為 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數的第一個參數值。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>備註

此值的型別為 **REG \_ SZ**。 它會與 [**DllSurrogate**](dllsurrogate.md) 值搭配使用，以避免在使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數時出現任何不明確的情況。 **DllSurrogate** 指出是否需要使用自訂代理，並將此資訊當做 **CreateProcess** 的第一個參數傳遞。 根據 **CreateProcess** 的執行，這項資訊可能不明確。 如果指定 **DllSurrogateExecutable** ，COM 會將此值傳遞為 **CreateProcess** 的第一個參數。 如果未指定 **DllSurrogateExecutable** ，COM 會傳遞 **Null** 做為 **CreateProcess** 第一個參數的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[DLL 代理](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 