---
title: IDXCoreAdapter::IsValid
description: 判斷這個 DXCore 介面卡物件是否仍然有效。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023854"
---
# <a name="idxcoreadapterisvalid-method"></a><span data-ttu-id="1b344-103">IDXCoreAdapter：： IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="1b344-103">IDXCoreAdapter::IsValid method</span></span>

<span data-ttu-id="1b344-104">判斷這個 DXCore 介面卡物件是否仍然有效。</span><span class="sxs-lookup"><span data-stu-id="1b344-104">Determines whether this DXCore adapter object is still valid.</span></span> <span data-ttu-id="1b344-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="1b344-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b344-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b344-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a><span data-ttu-id="1b344-107">傳回</span><span class="sxs-lookup"><span data-stu-id="1b344-107">Returns</span></span>

<span data-ttu-id="1b344-108">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="1b344-108">Type: **bool**</span></span>

<span data-ttu-id="1b344-109"> `true`   如果這個 DXCore 介面卡物件仍然有效，則會傳回。</span><span class="sxs-lookup"><span data-stu-id="1b344-109">Returns `true` if this DXCore adapter object is still valid.</span></span> <span data-ttu-id="1b344-110">否則，會傳回  `false` 。</span><span class="sxs-lookup"><span data-stu-id="1b344-110">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b344-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b344-111">See also</span></span>

<span data-ttu-id="1b344-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="1b344-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>