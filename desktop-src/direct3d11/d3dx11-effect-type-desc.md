---
title: 'D3DX11_EFFECT_TYPE_DESC 結構 (D3dx11effect .h) '
description: 描述效果變數型別。
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854064"
---
# <a name="d3dx11_effect_type_desc-structure"></a><span data-ttu-id="ed2c5-104">D3DX11 \_ 效果 \_ 類型 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="ed2c5-104">D3DX11\_EFFECT\_TYPE\_DESC structure</span></span>

<span data-ttu-id="ed2c5-105">描述效果變數型別。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-105">Describes an effect-variable type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2c5-106">語法</span><span class="sxs-lookup"><span data-stu-id="ed2c5-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a><span data-ttu-id="ed2c5-107">成員</span><span class="sxs-lookup"><span data-stu-id="ed2c5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed2c5-108">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-108">**TypeName**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-109">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-110">類型的名稱，例如 "float4" 或 "Mystruct>) "。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-110">Name of the type, for example "float4" or "MyStruct".</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-111">**類別**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-111">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-112">Type： **[ **D3D10 \_ 著色器 \_ 變數 \_ 類別**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-112">Type: **[**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-113">變數類別 (查看 [**D3D10 \_ 著色器 \_ 變數 \_ 類別**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)) 。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-113">The variable class (see [**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-114">**型別**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-114">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-115">類型： **[ **D3D10 \_ 著色器 \_ 變數 \_ 類型**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-115">Type: **[**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-116">變數型別 (查看 [**D3D10 \_ 著色器 \_ 變數 \_ 類型**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)) 。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-116">The variable type (see [**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-117">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-119">如果不是陣列) ，此類型中的元素數目 (0。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-119">Number of elements in this type (0 if not an array).</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-120">**成員**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-120">**Members**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-122">成員數目 (0 （如果不是結構) ）。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-122">Number of members (0 if not a structure).</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-123">**資料列**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-123">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-124">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-125">如果不是數值基本) ，此類型中的資料列數目 (0。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-125">Number of rows in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-126">**資料行**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-126">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-127">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-128">這種類型的資料行數目 (0 （如果不是數值基本) ）。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-128">Number of columns in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-129">**PackedSize**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-129">**PackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-130">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-131">當緊密壓縮時，表示此資料類型所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-131">Number of bytes required to represent this data type, when tightly packed.</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-132">**UnpackedSize**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-132">**UnpackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-133">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-134">在常數緩衝區中配置時，此資料類型所佔用的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-134">Number of bytes occupied by this data type, when laid out in a constant buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ed2c5-135">**分散**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-135">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="ed2c5-136">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed2c5-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ed2c5-137">在常數緩衝區中配置時，要在元素之間搜尋的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ed2c5-137">Number of bytes to seek between elements, when laid out in a constant buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed2c5-138">備註</span><span class="sxs-lookup"><span data-stu-id="ed2c5-138">Remarks</span></span>

<span data-ttu-id="ed2c5-139">D3DX11 \_ 效果 \_ 類型 \_ DESC 可搭配 [ **ID3DX11EffectType：： GetDesc** 使用](id3dx11effecttype-getdesc.md)</span><span class="sxs-lookup"><span data-stu-id="ed2c5-139">D3DX11\_EFFECT\_TYPE\_DESC is used with [**ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2c5-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed2c5-140">Requirements</span></span>



| <span data-ttu-id="ed2c5-141">需求</span><span class="sxs-lookup"><span data-stu-id="ed2c5-141">Requirement</span></span> | <span data-ttu-id="ed2c5-142">值</span><span class="sxs-lookup"><span data-stu-id="ed2c5-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2c5-143">標頭</span><span class="sxs-lookup"><span data-stu-id="ed2c5-143">Header</span></span><br/> | <dl> <span data-ttu-id="ed2c5-144"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed2c5-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed2c5-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed2c5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2c5-146">效果11結構</span><span class="sxs-lookup"><span data-stu-id="ed2c5-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

