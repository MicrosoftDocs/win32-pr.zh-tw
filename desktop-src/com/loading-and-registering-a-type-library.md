---
title: 載入和註冊類型程式庫
description: Automation 動態連結程式庫 Oleaut32.dll 可提供數個函式，您可以呼叫這些函式來載入和註冊類型程式庫。 如下列範例所示，呼叫 LoadTypeLibEx 會載入程式庫並建立登錄專案。
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98ea3a28f3884cbd6a377e45f1b537d169f510fdc4ce9a433dff6e976d9c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854228"
---
# <a name="loading-and-registering-a-type-library"></a>載入和註冊類型程式庫

Automation 動態連結程式庫 Oleaut32.dll 可提供數個函式，您可以呼叫這些函式來載入和註冊類型程式庫。 如下列範例所示，呼叫 [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex)會載入程式庫並建立登錄專案。

## <a name="example"></a>範例

``` syntax
ITypeLib *pTypeLib;
HRESULT hr;
hr = LoadTypeLibEx("example.tlb", REGKIND_REGISTER, &pTypeLib);
if(SUCCEEDED(hr))
{
    pTypeLib->Release();
} else {
    exit(0); // Handle errors here.
}
```

 

 