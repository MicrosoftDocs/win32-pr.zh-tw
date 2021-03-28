---
title: 'D3DX11_GROUP_DESC 結構 (D3dx11effect .h) '
description: 描述效果群組。
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035434"
---
# <a name="d3dx11_group_desc-structure"></a><span data-ttu-id="40a4e-104">D3DX11 \_ 群組 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="40a4e-104">D3DX11\_GROUP\_DESC structure</span></span>

<span data-ttu-id="40a4e-105">描述效果群組。</span><span class="sxs-lookup"><span data-stu-id="40a4e-105">Describes an effect group.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a4e-106">語法</span><span class="sxs-lookup"><span data-stu-id="40a4e-106">Syntax</span></span>


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a><span data-ttu-id="40a4e-107">成員</span><span class="sxs-lookup"><span data-stu-id="40a4e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="40a4e-108">**名稱**</span><span class="sxs-lookup"><span data-stu-id="40a4e-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="40a4e-109">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40a4e-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="40a4e-110">此群組的名稱 (只有在全域) 時才會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="40a4e-110">Name of this group (only **NULL** if global).</span></span>

</dd> <dt>

<span data-ttu-id="40a4e-111">**技術**</span><span class="sxs-lookup"><span data-stu-id="40a4e-111">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="40a4e-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40a4e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="40a4e-113">群組中包含的技術數目。</span><span class="sxs-lookup"><span data-stu-id="40a4e-113">Number of techniques contained in group.</span></span>

</dd> <dt>

<span data-ttu-id="40a4e-114">**註解**</span><span class="sxs-lookup"><span data-stu-id="40a4e-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="40a4e-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40a4e-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="40a4e-116">此群組的注釋數目。</span><span class="sxs-lookup"><span data-stu-id="40a4e-116">Number of annotations on this group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40a4e-117">備註</span><span class="sxs-lookup"><span data-stu-id="40a4e-117">Remarks</span></span>

<span data-ttu-id="40a4e-118">D3DX11 \_ GROUP \_ DESC 可與 [**ID3DX11EffectTechnique：： GetDesc**](id3dx11effecttechnique-getdesc.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="40a4e-118">D3DX11\_GROUP\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40a4e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="40a4e-119">Requirements</span></span>



| <span data-ttu-id="40a4e-120">需求</span><span class="sxs-lookup"><span data-stu-id="40a4e-120">Requirement</span></span> | <span data-ttu-id="40a4e-121">值</span><span class="sxs-lookup"><span data-stu-id="40a4e-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a4e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="40a4e-122">Header</span></span><br/> | <dl> <span data-ttu-id="40a4e-123"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="40a4e-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a4e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40a4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a4e-125">效果11結構</span><span class="sxs-lookup"><span data-stu-id="40a4e-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

