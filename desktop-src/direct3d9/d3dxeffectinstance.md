---
description: 用於管理一組預設效果參數的資料類型。
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: 'D3DXEFFECTINSTANCE 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322931"
---
# <a name="d3dxeffectinstance-structure"></a><span data-ttu-id="90988-103">D3DXEFFECTINSTANCE 結構</span><span class="sxs-lookup"><span data-stu-id="90988-103">D3DXEFFECTINSTANCE structure</span></span>

<span data-ttu-id="90988-104">用於管理一組預設效果參數的資料類型。</span><span class="sxs-lookup"><span data-stu-id="90988-104">Data type for managing a set of default effect parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="90988-105">語法</span><span class="sxs-lookup"><span data-stu-id="90988-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a><span data-ttu-id="90988-106">成員</span><span class="sxs-lookup"><span data-stu-id="90988-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="90988-107">**pEffectFilename**</span><span class="sxs-lookup"><span data-stu-id="90988-107">**pEffectFilename**</span></span>
</dt> <dd>

<span data-ttu-id="90988-108">類型： **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="90988-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="90988-109">效果檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="90988-109">Name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="90988-110">**NumDefaults**</span><span class="sxs-lookup"><span data-stu-id="90988-110">**NumDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="90988-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90988-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90988-112">預設參數的數目。</span><span class="sxs-lookup"><span data-stu-id="90988-112">Number of default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="90988-113">**pDefaults**</span><span class="sxs-lookup"><span data-stu-id="90988-113">**pDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="90988-114">類型： **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span><span class="sxs-lookup"><span data-stu-id="90988-114">Type: **[**LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90988-115">[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)元素陣列的指標，其中每個專案都包含效果參數。</span><span class="sxs-lookup"><span data-stu-id="90988-115">Pointer to an array of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) elements, each of which contains an effect parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90988-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="90988-116">Requirements</span></span>



| <span data-ttu-id="90988-117">需求</span><span class="sxs-lookup"><span data-stu-id="90988-117">Requirement</span></span> | <span data-ttu-id="90988-118">值</span><span class="sxs-lookup"><span data-stu-id="90988-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90988-119">標頭</span><span class="sxs-lookup"><span data-stu-id="90988-119">Header</span></span><br/> | <dl> <span data-ttu-id="90988-120"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="90988-120"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90988-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90988-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90988-122">效果結構</span><span class="sxs-lookup"><span data-stu-id="90988-122">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
