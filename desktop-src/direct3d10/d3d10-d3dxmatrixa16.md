---
description: 4x4、16位元組對齊的矩陣，其中包含方法和運算子多載。
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: 'D3DXMATRIXA16 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a33b5efa0e5e714c0b161fed8191702066a44b01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196410"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a><span data-ttu-id="96a83-103">D3DXMATRIXA16 結構 (D3DX10Math .h) </span><span class="sxs-lookup"><span data-stu-id="96a83-103">D3DXMATRIXA16 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="96a83-104">4x4、16位元組對齊的矩陣，其中包含方法和運算子多載。</span><span class="sxs-lookup"><span data-stu-id="96a83-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a83-105">語法</span><span class="sxs-lookup"><span data-stu-id="96a83-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="96a83-106">成員</span><span class="sxs-lookup"><span data-stu-id="96a83-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96a83-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="96a83-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="96a83-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96a83-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96a83-109">矩陣的 (i，j) 元件，其中 i 是資料列編號，而 j 是資料行編號。</span><span class="sxs-lookup"><span data-stu-id="96a83-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="96a83-110">例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。</span><span class="sxs-lookup"><span data-stu-id="96a83-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96a83-111">備註</span><span class="sxs-lookup"><span data-stu-id="96a83-111">Remarks</span></span>

<span data-ttu-id="96a83-112">D3DX 數學函式使用時，16位元組對齊的矩陣已經過優化，以改善 Intel Pentium 4 處理器的效能。</span><span class="sxs-lookup"><span data-stu-id="96a83-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="96a83-113">矩陣的對齊方式與它們的建立位置無關：在程式堆疊上、堆積或全域範圍中。</span><span class="sxs-lookup"><span data-stu-id="96a83-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="96a83-114">您可以使用 \_ \_ declspec (對齊 (16) ) 來完成對齊，這項功能僅適用于 Visual C++ .net，而且只有在安裝處理器套件時才會使用 Visual C++ 6.0。</span><span class="sxs-lookup"><span data-stu-id="96a83-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="96a83-115">可惜的是，沒有任何方法可以偵測處理器套件，因此預設只會根據 Visual C++ .NET 來開啟位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="96a83-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="96a83-116">向量和四元數在 D3DX 中不是位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="96a83-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="96a83-117">搭配使用向量和四元數與 D3DX 數學函式時，請使用 \_ declspec (對齊 (16) ) 來產生位元組對齊的向量和四元數，因為它們的執行效能大幅提升。</span><span class="sxs-lookup"><span data-stu-id="96a83-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="96a83-118">Declspec 的定義 \_ 如下所示。</span><span class="sxs-lookup"><span data-stu-id="96a83-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="96a83-119">其他編譯器會將 **D3DXMATRIXA16** 解讀為 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="96a83-119">Other compilers interpret **D3DXMATRIXA16** as [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span> <span data-ttu-id="96a83-120">在未實際對齊矩陣的編譯器上使用此結構可能會造成問題，因為它不會公開會忽略對齊的 bug。</span><span class="sxs-lookup"><span data-stu-id="96a83-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="96a83-121">例如，如果 **D3DXMATRIXA16** 物件位於結構或類別內，則可能會使用緊密封裝完成 [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) ， (忽略16位元組界限) 。</span><span class="sxs-lookup"><span data-stu-id="96a83-121">For example, if a **D3DXMATRIXA16** object is inside a structure or class, a [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="96a83-122">如果編譯器在一段時間加入矩陣時，這會造成組建中斷。</span><span class="sxs-lookup"><span data-stu-id="96a83-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16-extensions"></a><span data-ttu-id="96a83-123">D3DXMATRIXA16 延伸模組</span><span class="sxs-lookup"><span data-stu-id="96a83-123">D3DXMATRIXA16 Extensions</span></span>

<span data-ttu-id="96a83-124">**D3DXMATRIXA16** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="96a83-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a><span data-ttu-id="96a83-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="96a83-125">Requirements</span></span>



| <span data-ttu-id="96a83-126">需求</span><span class="sxs-lookup"><span data-stu-id="96a83-126">Requirement</span></span> | <span data-ttu-id="96a83-127">值</span><span class="sxs-lookup"><span data-stu-id="96a83-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96a83-128">標頭</span><span class="sxs-lookup"><span data-stu-id="96a83-128">Header</span></span><br/> | <dl> <span data-ttu-id="96a83-129"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="96a83-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a83-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96a83-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a83-131">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="96a83-131">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
