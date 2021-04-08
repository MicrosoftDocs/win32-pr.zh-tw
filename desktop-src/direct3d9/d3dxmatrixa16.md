---
description: 4x4、16位元組對齊的矩陣，其中包含方法和運算子多載。
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: 'D3DXMATRIXA16 結構 (D3dx9math .h) '
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
- d3dx9math.h
ms.openlocfilehash: 57d2e5e796b929c87d4724d298758f26088918c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696615"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a><span data-ttu-id="059d7-103">D3DXMATRIXA16 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="059d7-103">D3DXMATRIXA16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="059d7-104">4x4、16位元組對齊的矩陣，其中包含方法和運算子多載。</span><span class="sxs-lookup"><span data-stu-id="059d7-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="059d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="059d7-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="059d7-106">成員</span><span class="sxs-lookup"><span data-stu-id="059d7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="059d7-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="059d7-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="059d7-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="059d7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="059d7-109">矩陣的 (i，j) 元件，其中 i 是資料列編號，而 j 是資料行編號。</span><span class="sxs-lookup"><span data-stu-id="059d7-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="059d7-110">例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。</span><span class="sxs-lookup"><span data-stu-id="059d7-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="059d7-111">備註</span><span class="sxs-lookup"><span data-stu-id="059d7-111">Remarks</span></span>

<span data-ttu-id="059d7-112">D3DX 數學函式使用時，16位元組對齊的矩陣已經過優化，以改善 Intel Pentium 4 處理器的效能。</span><span class="sxs-lookup"><span data-stu-id="059d7-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="059d7-113">矩陣的對齊方式與它們的建立位置無關：在程式堆疊上、堆積或全域範圍中。</span><span class="sxs-lookup"><span data-stu-id="059d7-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="059d7-114">您可以使用 \_ \_ declspec (對齊 (16) ) 來完成對齊，這項功能僅適用于 Visual C++ .net，而且只有在安裝處理器套件時才會使用 Visual C++ 6.0。</span><span class="sxs-lookup"><span data-stu-id="059d7-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="059d7-115">可惜的是，沒有任何方法可以偵測處理器套件，因此預設只會根據 Visual C++ .NET 來開啟位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="059d7-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="059d7-116">向量和四元數在 D3DX 中不是位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="059d7-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="059d7-117">搭配使用向量和四元數與 D3DX 數學函式時，請使用 \_ declspec (對齊 (16) ) 來產生位元組對齊的向量和四元數，因為它們的執行效能大幅提升。</span><span class="sxs-lookup"><span data-stu-id="059d7-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="059d7-118">Declspec 的定義 \_ 如下所示。</span><span class="sxs-lookup"><span data-stu-id="059d7-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="059d7-119">其他編譯器會將 D3DXMATRIXA16 解讀為 D3DXMATRIX。</span><span class="sxs-lookup"><span data-stu-id="059d7-119">Other compilers interpret D3DXMATRIXA16 as D3DXMATRIX.</span></span> <span data-ttu-id="059d7-120">在未實際對齊矩陣的編譯器上使用此結構可能會造成問題，因為它不會公開會忽略對齊的 bug。</span><span class="sxs-lookup"><span data-stu-id="059d7-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="059d7-121">例如，如果 D3DXMATRIXA16 物件位於結構或類別內，則可能會使用緊密封裝完成 [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) ， (忽略16位元組界限) 。</span><span class="sxs-lookup"><span data-stu-id="059d7-121">For example, if a D3DXMATRIXA16 object is inside a structure or class, a [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="059d7-122">如果編譯器在一段時間加入矩陣時，這會造成組建中斷。</span><span class="sxs-lookup"><span data-stu-id="059d7-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16"></a><span data-ttu-id="059d7-123">D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="059d7-123">D3DXMATRIXA16</span></span>

<span data-ttu-id="059d7-124">**D3DXMATRIXA16** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="059d7-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="059d7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="059d7-125">Requirements</span></span>



| <span data-ttu-id="059d7-126">需求</span><span class="sxs-lookup"><span data-stu-id="059d7-126">Requirement</span></span> | <span data-ttu-id="059d7-127">值</span><span class="sxs-lookup"><span data-stu-id="059d7-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="059d7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="059d7-128">Header</span></span><br/> | <dl> <span data-ttu-id="059d7-129"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="059d7-129"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="059d7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="059d7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="059d7-131">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="059d7-131">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="059d7-132">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="059d7-132">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> </dl>

 

 
