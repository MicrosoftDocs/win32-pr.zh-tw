---
title: IDXCoreAdapterList::GetAdapterCount
description: 捕獲 DXCore 介面卡清單物件中的介面卡數目。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 067e7046d53bdd63f3c8db0c856cf5664a09f426
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186094"
---
# <a name="idxcoreadapterlistgetadaptercount-method"></a><span data-ttu-id="66980-103">IDXCoreAdapterList：： GetAdapterCount 方法</span><span class="sxs-lookup"><span data-stu-id="66980-103">IDXCoreAdapterList::GetAdapterCount method</span></span>

<span data-ttu-id="66980-104">捕獲 DXCore 介面卡清單物件中的介面卡數目。</span><span class="sxs-lookup"><span data-stu-id="66980-104">Retrieves the number of adapters in a DXCore adapter list object.</span></span> <span data-ttu-id="66980-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="66980-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="66980-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="66980-106">Syntax</span></span>

```cpp
virtual uint32_t STDMETHODCALLTYPE GetAdapterCount() = 0;
```

## <a name="returns"></a><span data-ttu-id="66980-107">傳回</span><span class="sxs-lookup"><span data-stu-id="66980-107">Returns</span></span>

<span data-ttu-id="66980-108">類型： **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="66980-108">Type: **uint32_t**</span></span>

<span data-ttu-id="66980-109">傳回清單中的介面卡專案數目。</span><span class="sxs-lookup"><span data-stu-id="66980-109">Returns the number of adapter items in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="66980-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66980-110">See also</span></span>

<span data-ttu-id="66980-111">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="66980-111">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>