---
description: 將物件宣告為挑選任何常數，以避免在 DirectXMath 程式庫的多個位置中，將該物件的重複重載用於 (和宣告) 。
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST 宏
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998084"
---
# <a name="xmglobalconst-macro"></a><span data-ttu-id="8c54e-103">XMGLOBALCONST 宏</span><span class="sxs-lookup"><span data-stu-id="8c54e-103">XMGLOBALCONST macro</span></span>

<span data-ttu-id="8c54e-104">將物件宣告為 *挑選任何* 常數，以避免在 DirectXMath 程式庫的多個位置中，將該物件的重複重載用於 (和宣告) 。</span><span class="sxs-lookup"><span data-stu-id="8c54e-104">Declares an object to be a *pick-any* constant, to avoid redundant reloads of that object if it is used (and declared) in multiple places in the DirectXMath Library.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c54e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c54e-105">Syntax</span></span>

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a><span data-ttu-id="8c54e-106">備註</span><span class="sxs-lookup"><span data-stu-id="8c54e-106">Remarks</span></span>

<span data-ttu-id="8c54e-107">使用 XMGLOBALCONST 允許全域常數的規格。</span><span class="sxs-lookup"><span data-stu-id="8c54e-107">Using XMGLOBALCONST permits the specification of global constants.</span></span> <span data-ttu-id="8c54e-108">這有助於減少應用程式資料區段的大小、避免重複的物件建立和損毀，並減少載入和儲存作業。</span><span class="sxs-lookup"><span data-stu-id="8c54e-108">This helps to reduce the size of an application's data segment, avoid redundant object creation and destruction, and reduce load and store operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c54e-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c54e-109">Requirements</span></span>

<span data-ttu-id="8c54e-110">**標頭：** 在 DirectXMath 中宣告。</span><span class="sxs-lookup"><span data-stu-id="8c54e-110">**Header:** Declared in DirectXMath.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c54e-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c54e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c54e-112">DirectXMath 程式庫宏</span><span class="sxs-lookup"><span data-stu-id="8c54e-112">DirectXMath Library Macros</span></span>](ovw-xnamath-reference-macros.md)
</dt> <dt>

[<span data-ttu-id="8c54e-113">DirectXMath 程式庫中的全域常數</span><span class="sxs-lookup"><span data-stu-id="8c54e-113">Global Constants in the DirectXMath Library</span></span>](pg-xnamath-internals.md)
</dt> <dt>

<span data-ttu-id="8c54e-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="8c54e-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span></span>
</dt> <dt>

<span data-ttu-id="8c54e-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="8c54e-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span></span>
</dt> </dl>

 

 
