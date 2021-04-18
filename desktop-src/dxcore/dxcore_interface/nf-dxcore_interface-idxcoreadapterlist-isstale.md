---
title: IDXCoreAdapterList::IsStale
description: 判斷此系統的變更是否造成此 DXCore 介面卡清單物件過期。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965451"
---
# <a name="idxcoreadapterlistisstale-method"></a><span data-ttu-id="f972d-103">IDXCoreAdapterList：： IsStale 方法</span><span class="sxs-lookup"><span data-stu-id="f972d-103">IDXCoreAdapterList::IsStale method</span></span>

<span data-ttu-id="f972d-104">判斷此系統的變更是否造成此 DXCore 介面卡清單物件過期。</span><span class="sxs-lookup"><span data-stu-id="f972d-104">Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.</span></span> <span data-ttu-id="f972d-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="f972d-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f972d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f972d-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a><span data-ttu-id="f972d-107">傳回</span><span class="sxs-lookup"><span data-stu-id="f972d-107">Returns</span></span>

<span data-ttu-id="f972d-108">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="f972d-108">Type: **bool**</span></span>

<span data-ttu-id="f972d-109"> `true`   如果產生清單，則會傳回系統狀況的變更，使此介面卡清單變成過時。</span><span class="sxs-lookup"><span data-stu-id="f972d-109">Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale.</span></span> <span data-ttu-id="f972d-110">否則，會傳回  `false` 。</span><span class="sxs-lookup"><span data-stu-id="f972d-110">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f972d-111">備註</span><span class="sxs-lookup"><span data-stu-id="f972d-111">Remarks</span></span>

<span data-ttu-id="f972d-112">您可以輪詢 **IsStale** ，以判斷變更的系統條件是否會導致此清單變成過期。</span><span class="sxs-lookup"><span data-stu-id="f972d-112">You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date.</span></span> <span data-ttu-id="f972d-113">如果 **IsStale** 傳回 `true` 一次，則會傳回 `true` DXCore 介面卡清單物件的剩餘存留期。</span><span class="sxs-lookup"><span data-stu-id="f972d-113">If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object.</span></span> <span data-ttu-id="f972d-114">即使系統條件返回符合清單的狀態，也會將過時的清單物件視為過時， (相同的條件會立即取得，就像是首次產生清單一樣) 。</span><span class="sxs-lookup"><span data-stu-id="f972d-114">A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).</span></span>

## <a name="see-also"></a><span data-ttu-id="f972d-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f972d-115">See also</span></span>

<span data-ttu-id="f972d-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f972d-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>