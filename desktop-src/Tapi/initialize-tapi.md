---
description: 下列程式碼範例將示範如何建立 TAPI 物件。
ms.assetid: f8566e53-51c9-4424-a8bb-369455f35706
title: 初始化 TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78062e71df2d68895a645ca8a6c4c480a1415cd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852043"
---
# <a name="initialize-tapi"></a><span data-ttu-id="663e2-103">初始化 TAPI</span><span class="sxs-lookup"><span data-stu-id="663e2-103">Initialize TAPI</span></span>

<span data-ttu-id="663e2-104">下列程式碼範例將示範如何建立 TAPI 物件。</span><span class="sxs-lookup"><span data-stu-id="663e2-104">The following code example demonstrates creation of the TAPI object.</span></span>

```cpp
const auto result = ITTAPI::Initialize();

if (result != S_OK) {
    switch (result) {
        case S_FALSE: {
            std::cerr << "TAPI has already been initialized.\n";
        } break;

        [[fallthrough]]
        case E_OUTOFMEMORY: {
            std::cerr << "Insufficient memory exists to perform the operation.\n";
        }

        default: {
            // TODO: Handle unrecoverable error here
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="663e2-105">另請參閱</span><span class="sxs-lookup"><span data-stu-id="663e2-105">See Also</span></span>

- [<span data-ttu-id="663e2-106">ITTAPI：： Initialize</span><span class="sxs-lookup"><span data-stu-id="663e2-106">ITTAPI::Initialize</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-initialize)
- [<span data-ttu-id="663e2-107">一般 HRESULT 值</span><span class="sxs-lookup"><span data-stu-id="663e2-107">Common HRESULT Values</span></span>](../seccrypto/common-hresult-values.md)
