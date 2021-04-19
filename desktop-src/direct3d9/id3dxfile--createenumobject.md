---
description: 建立將讀取 x.x 檔案的列舉值物件。
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile：： CreateEnumObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975692"
---
# <a name="id3dxfilecreateenumobject-method"></a><span data-ttu-id="81734-103">ID3DXFile：： CreateEnumObject 方法</span><span class="sxs-lookup"><span data-stu-id="81734-103">ID3DXFile::CreateEnumObject method</span></span>

<span data-ttu-id="81734-104">建立將讀取 x.x 檔案的列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="81734-104">Creates an enumerator object that will read a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="81734-105">語法</span><span class="sxs-lookup"><span data-stu-id="81734-105">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="81734-106">參數</span><span class="sxs-lookup"><span data-stu-id="81734-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81734-107">*pvSource* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81734-107">*pvSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81734-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81734-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81734-109">資料來源。</span><span class="sxs-lookup"><span data-stu-id="81734-109">The data source.</span></span> <span data-ttu-id="81734-110">任一：</span><span class="sxs-lookup"><span data-stu-id="81734-110">Either:</span></span>

-   <span data-ttu-id="81734-111">檔案名</span><span class="sxs-lookup"><span data-stu-id="81734-111">A file name</span></span>
-   <span data-ttu-id="81734-112">[**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)結構</span><span class="sxs-lookup"><span data-stu-id="81734-112">A [**D3DXF\_FILELOADMEMORY**](d3dxf-fileloadmemory.md) structure</span></span>
-   <span data-ttu-id="81734-113">[**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)結構</span><span class="sxs-lookup"><span data-stu-id="81734-113">A [**D3DXF\_FILELOADRESOURCE**](d3dxf-fileloadresource.md) structure</span></span>

<span data-ttu-id="81734-114">取決於 loadflags 的值。</span><span class="sxs-lookup"><span data-stu-id="81734-114">Depending on the value of loadflags.</span></span>

</dd> <dt>

<span data-ttu-id="81734-115">*loadflags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81734-115">*loadflags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81734-116">類型： **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="81734-116">Type: **[D3DXF\_FILELOADOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="81734-117">指定資料來源的值。</span><span class="sxs-lookup"><span data-stu-id="81734-117">Value that specifies the source of the data.</span></span> <span data-ttu-id="81734-118">這個值可以是其中一個 [D3DXF \_ FILELOADOPTIONS](d3dxf.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="81734-118">This value can be one of the [D3DXF\_FILELOADOPTIONS](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="81734-119">*ppEnumObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81734-119">*ppEnumObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81734-120">類型： **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="81734-120">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="81734-121">[**ID3DXFileEnumObject**](id3dxfileenumobject.md)介面指標的位址，表示已建立的枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="81734-121">Address of a pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81734-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="81734-122">Return value</span></span>

<span data-ttu-id="81734-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81734-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81734-124">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="81734-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="81734-125">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE，D3DXFERR \_ PARSEERROR。</span><span class="sxs-lookup"><span data-stu-id="81734-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="81734-126">備註</span><span class="sxs-lookup"><span data-stu-id="81734-126">Remarks</span></span>

<span data-ttu-id="81734-127">使用這個方法之後，請使用其中一個 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 方法來取出資料物件。</span><span class="sxs-lookup"><span data-stu-id="81734-127">After using this method, use one of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="81734-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="81734-128">Requirements</span></span>



| <span data-ttu-id="81734-129">需求</span><span class="sxs-lookup"><span data-stu-id="81734-129">Requirement</span></span> | <span data-ttu-id="81734-130">值</span><span class="sxs-lookup"><span data-stu-id="81734-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81734-131">標頭</span><span class="sxs-lookup"><span data-stu-id="81734-131">Header</span></span><br/>  | <dl> <span data-ttu-id="81734-132"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="81734-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="81734-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="81734-133">Library</span></span><br/> | <dl> <span data-ttu-id="81734-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="81734-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="81734-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81734-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81734-136">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="81734-136">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="81734-137">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="81734-137">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
