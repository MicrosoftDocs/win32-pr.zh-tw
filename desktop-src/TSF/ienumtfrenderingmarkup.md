---
title: IEnumTfRenderingMarkup 介面
description: IEnumTfRenderingMarkup 介面是由 TSF 管理員所執行，並由應用程式使用。 此介面可透過 ITfCoNtextRenderingMarkup GetRenderingMarkup 來抓取，並列舉轉譯標記資訊。
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- IEnumTfRenderingMarkup 介面文字服務架構
- IEnumTfRenderingMarkup 介面文字服務架構，說明
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023887"
---
# <a name="ienumtfrenderingmarkup-interface"></a><span data-ttu-id="43d46-106">IEnumTfRenderingMarkup 介面</span><span class="sxs-lookup"><span data-stu-id="43d46-106">IEnumTfRenderingMarkup interface</span></span>

<span data-ttu-id="43d46-107">**IEnumTfRenderingMarkup** 介面是由 TSF 管理員所執行，並由應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="43d46-107">The **IEnumTfRenderingMarkup** interface is implemented by TSF Manager and used by applications.</span></span> <span data-ttu-id="43d46-108">此介面可由 [ITfCoNtextRenderingMarkup：： GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) 抓取，並列舉轉譯標記資訊。</span><span class="sxs-lookup"><span data-stu-id="43d46-108">This interface can be retrieved by [ITfContextRenderingMarkup::GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) and enumerates the rendering markup information.</span></span>



| <span data-ttu-id="43d46-109">IEnumTfRenderingMarkup 方法</span><span class="sxs-lookup"><span data-stu-id="43d46-109">IEnumTfRenderingMarkup methods</span></span>            | <span data-ttu-id="43d46-110">Description</span><span class="sxs-lookup"><span data-stu-id="43d46-110">Description</span></span>                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43d46-111">複製</span><span class="sxs-lookup"><span data-stu-id="43d46-111">Clone</span></span>](ienumtfrenderingmarkup-clone.md) | <span data-ttu-id="43d46-112">**IEnumTfRenderingMarkup：： Clone** 方法會建立枚舉器物件的複本。</span><span class="sxs-lookup"><span data-stu-id="43d46-112">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>                                                                  |
| [<span data-ttu-id="43d46-113">下一步</span><span class="sxs-lookup"><span data-stu-id="43d46-113">Next</span></span>](ienumtfrenderingmarkup-next.md)   | <span data-ttu-id="43d46-114">**IEnumTfRenderingMarkup：： Next** 方法會從目前位置取得列舉順序中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="43d46-114">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |
| [<span data-ttu-id="43d46-115">重設</span><span class="sxs-lookup"><span data-stu-id="43d46-115">Reset</span></span>](ienumtfrenderingmarkup-reset.md) | <span data-ttu-id="43d46-116">**IEnumTfRenderingMarkup：： Reset** 方法會將目前的位置移至列舉序列的開頭，以重設列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="43d46-116">The **IEnumTfRenderingMarkup::Reset** method resets the enumerator object by moving the current position to the beginning of the enumeration sequence.</span></span> |
| [<span data-ttu-id="43d46-117">Skip</span><span class="sxs-lookup"><span data-stu-id="43d46-117">Skip</span></span>](ienumtfrenderingmarkup-skip.md)   | <span data-ttu-id="43d46-118">**IEnumTfRenderingMarkup：： Skip** 方法會從目前位置取得列舉順序中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="43d46-118">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |



 

## <a name="members"></a><span data-ttu-id="43d46-119">成員</span><span class="sxs-lookup"><span data-stu-id="43d46-119">Members</span></span>

<span data-ttu-id="43d46-120">**IEnumTfRenderingMarkup** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="43d46-120">The **IEnumTfRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d46-121">備註</span><span class="sxs-lookup"><span data-stu-id="43d46-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43d46-122">這個介面目前不在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="43d46-122">This interface is not currently in the public header files.</span></span> <span data-ttu-id="43d46-123">若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="43d46-123">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 