---
description: 描述效果所使用的函數。
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: 'D3DXFUNCTION_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000593"
---
# <a name="d3dxfunction_desc-structure"></a><span data-ttu-id="7a26b-103">D3DXFUNCTION \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="7a26b-103">D3DXFUNCTION\_DESC structure</span></span>

<span data-ttu-id="7a26b-104">描述效果所使用的函數。</span><span class="sxs-lookup"><span data-stu-id="7a26b-104">Describes a function used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a26b-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a26b-105">Syntax</span></span>


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a><span data-ttu-id="7a26b-106">成員</span><span class="sxs-lookup"><span data-stu-id="7a26b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a26b-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7a26b-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="7a26b-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a26b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a26b-109">函式名稱。</span><span class="sxs-lookup"><span data-stu-id="7a26b-109">Function name.</span></span>

</dd> <dt>

<span data-ttu-id="7a26b-110">**註解**</span><span class="sxs-lookup"><span data-stu-id="7a26b-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="7a26b-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a26b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a26b-112">未使用的。</span><span class="sxs-lookup"><span data-stu-id="7a26b-112">Unused.</span></span> <span data-ttu-id="7a26b-113">[**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)一律會將這個成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="7a26b-113">This member will always be set to zero by [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a26b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a26b-114">Requirements</span></span>



| <span data-ttu-id="7a26b-115">需求</span><span class="sxs-lookup"><span data-stu-id="7a26b-115">Requirement</span></span> | <span data-ttu-id="7a26b-116">值</span><span class="sxs-lookup"><span data-stu-id="7a26b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a26b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7a26b-117">Header</span></span><br/> | <dl> <span data-ttu-id="7a26b-118"><dt>D3dx9effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a26b-118"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a26b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a26b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a26b-120">效果結構</span><span class="sxs-lookup"><span data-stu-id="7a26b-120">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
