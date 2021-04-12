---
title: IDXCoreAdapter
description: " **IDXCoreAdapter**   介面會執行方法，以取得介面卡專案的詳細資料。"
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093152"
---
# <a name="idxcoreadapter-interface"></a><span data-ttu-id="d4969-103">IDXCoreAdapter 介面</span><span class="sxs-lookup"><span data-stu-id="d4969-103">IDXCoreAdapter interface</span></span>

<span data-ttu-id="d4969-104"> **IDXCoreAdapter**   介面會執行方法，以取得介面卡專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d4969-104">The **IDXCoreAdapter** interface implements methods for retrieving details about an adapter item.</span></span> <span data-ttu-id="d4969-105">**IDXCoreAdapter** 繼承自 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。</span><span class="sxs-lookup"><span data-stu-id="d4969-105">**IDXCoreAdapter** inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d4969-106">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="d4969-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4969-107">備註</span><span class="sxs-lookup"><span data-stu-id="d4969-107">Remarks</span></span>

<span data-ttu-id="d4969-108">介面卡的屬性會在介面卡啟動時建立，而且在介面卡的存留期內是不可變的。</span><span class="sxs-lookup"><span data-stu-id="d4969-108">An adapter's properties are established at the time the adapter starts, and they're immutable for the lifetime of the adapter.</span></span> <span data-ttu-id="d4969-109">這與可查詢或設定的介面卡狀態不同，而其值可能會隨著時間而變更。</span><span class="sxs-lookup"><span data-stu-id="d4969-109">This is in contrast to an adapter's state, which can be queried or set, and the values of which can change over time.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4969-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4969-110">See also</span></span>

<span data-ttu-id="d4969-111">[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="d4969-111">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>