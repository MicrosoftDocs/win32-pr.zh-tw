---
description: 定義可啟用使用者定義裁剪平面的位模式。 在設定 D3DRS CLIPPLANEENABLE 轉譯狀態的值時，會定義這些宏的便利性 \_ 。
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: 'D3DCLIPPLANEn 宏 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386438"
---
# <a name="d3dclipplanen-macro"></a><span data-ttu-id="0fe4d-104">D3DCLIPPLANEn 宏</span><span class="sxs-lookup"><span data-stu-id="0fe4d-104">D3DCLIPPLANEn macro</span></span>

<span data-ttu-id="0fe4d-105">定義可啟用使用者定義裁剪平面的位模式。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-105">Defines bit patterns that enable user-defined clipping planes.</span></span> <span data-ttu-id="0fe4d-106">在設定 D3DRS CLIPPLANEENABLE 轉譯狀態的值時，會定義這些宏的便利性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-106">These macros are defined as a convenience when setting values for the D3DRS\_CLIPPLANEENABLE render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe4d-107">語法</span><span class="sxs-lookup"><span data-stu-id="0fe4d-107">Syntax</span></span>


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a><span data-ttu-id="0fe4d-108">參數</span><span class="sxs-lookup"><span data-stu-id="0fe4d-108">Parameters</span></span>

<span data-ttu-id="0fe4d-109">這個宏沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-109">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fe4d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fe4d-110">Return value</span></span>

<span data-ttu-id="0fe4d-111">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-111">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe4d-112">備註</span><span class="sxs-lookup"><span data-stu-id="0fe4d-112">Remarks</span></span>

<span data-ttu-id="0fe4d-113">當 D3DRS CLIPPLANEENABLE 轉譯狀態中設定的值 \_ 包含一或多個設定的位 (也就是不是 0) 時，會啟用使用者定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-113">User-defined clipping planes are enabled when the value set in the D3DRS\_CLIPPLANEENABLE render state contains one or more set bits (that is, is not 0).</span></span> <span data-ttu-id="0fe4d-114">轉譯狀態的值並不重要;系統不會將值轉譯為數字。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-114">The value of the render-state is not important; the system does not interpret the value as a number.</span></span> <span data-ttu-id="0fe4d-115">相反地，此值會啟用對應位已設定的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-115">Rather, the value enables the clipping plane whose corresponding bit is set.</span></span> <span data-ttu-id="0fe4d-116">Bit 0 控制第一個裁剪平面的狀態 (在索引 0) 、位1第二個平面等等。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-116">Bit 0 controls the state of the first clipping plane (at index 0), bit 1 the second plane, and so on.</span></span>

<span data-ttu-id="0fe4d-117">您可以使用邏輯 OR 運算來結合這些宏所建立的位模式，以同時啟用多個裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-117">The bit patterns that these macros create can be combined by using a logical OR operation to simultaneously enable multiple clipping planes.</span></span> <span data-ttu-id="0fe4d-118">從組合中省略上述其中一個宏，實際上會停用該索引的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="0fe4d-118">Omitting one of these macros from the combination effectively disables the clipping plane at that index.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe4d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fe4d-119">Requirements</span></span>



| <span data-ttu-id="0fe4d-120">需求</span><span class="sxs-lookup"><span data-stu-id="0fe4d-120">Requirement</span></span> | <span data-ttu-id="0fe4d-121">值</span><span class="sxs-lookup"><span data-stu-id="0fe4d-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe4d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0fe4d-122">Header</span></span><br/> | <dl> <span data-ttu-id="0fe4d-123"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fe4d-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe4d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fe4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe4d-125">巨集</span><span class="sxs-lookup"><span data-stu-id="0fe4d-125">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




