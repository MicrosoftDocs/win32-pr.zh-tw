---
title: 載入和註冊類型程式庫
description: Automation 動態連結程式庫 Oleaut32.dll 可提供數個函式，您可以呼叫這些函式來載入和註冊類型程式庫。 如下列範例所示，呼叫 LoadTypeLibEx 會載入程式庫並建立登錄專案。
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d533225913d6bcfbb74df3ac42bd00b18b00e4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024208"
---
# <a name="loading-and-registering-a-type-library"></a><span data-ttu-id="2f36b-104">載入和註冊類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2f36b-104">Loading and Registering a Type Library</span></span>

<span data-ttu-id="2f36b-105">Automation 動態連結程式庫 Oleaut32.dll 可提供數個函式，您可以呼叫這些函式來載入和註冊類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="2f36b-105">The Automation dynamic link library, Oleaut32.dll, provides several functions that you can call to load and register a type library.</span></span> <span data-ttu-id="2f36b-106">如下列範例所示，呼叫 [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex)會載入程式庫並建立登錄專案。</span><span class="sxs-lookup"><span data-stu-id="2f36b-106">Calling [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), as shown in the following example, both loads the library and creates the registry entries.</span></span>

## <a name="example"></a><span data-ttu-id="2f36b-107">範例</span><span class="sxs-lookup"><span data-stu-id="2f36b-107">Example</span></span>

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

 

 