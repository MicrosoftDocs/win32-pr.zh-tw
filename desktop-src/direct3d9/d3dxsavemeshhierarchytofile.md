---
description: 建立 x.x 檔案，並在其中儲存網格階層和對應的動畫。
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: 'D3DXSaveMeshHierarchyToFile 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985530"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a><span data-ttu-id="2a1fa-103">D3DXSaveMeshHierarchyToFile 函式</span><span class="sxs-lookup"><span data-stu-id="2a1fa-103">D3DXSaveMeshHierarchyToFile function</span></span>

<span data-ttu-id="2a1fa-104">建立 x.x 檔案，並在其中儲存網格階層和對應的動畫。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-104">Creates a .x file and saves the mesh hierarchy and corresponding animations in it.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a1fa-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a><span data-ttu-id="2a1fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a1fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a1fa-107">*pFilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a1fa-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1fa-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1fa-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a1fa-109">字串的指標，這個字串會指定識別已儲存網格的. x 檔案名。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-109">Pointer to a string that specifies the name of the .x file identifying the saved mesh.</span></span> <span data-ttu-id="2a1fa-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2a1fa-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2a1fa-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2a1fa-113">*XFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a1fa-113">*XFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1fa-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1fa-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a1fa-115">. X 檔案的格式 (文字或二進位檔案、壓縮或不) 。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-115">Format of the .x file (text or binary, compressed or not).</span></span> <span data-ttu-id="2a1fa-116">請參閱 D3DXF \_ >fileformat。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-116">See D3DXF\_FILEFORMAT.</span></span> <span data-ttu-id="2a1fa-117">您 \_ \_ 可以將 D3DXF >fileformat 壓縮 (使用邏輯 OR) 搭配 D3DXF \_ >FILEFORMAT \_ BINARY 或 D3DXF \_ >fileformat \_ 文字旗標，以縮減輸出檔案大小。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-117">D3DXF\_FILEFORMAT\_COMPRESSED can be combined (using a logical OR) with either the D3DXF\_FILEFORMAT\_BINARY or D3DXF\_FILEFORMAT\_TEXT flags to reduce the output file size.</span></span>

</dd> <dt>

<span data-ttu-id="2a1fa-118">*pFrameRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a1fa-118">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1fa-119">Type： **Const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a1fa-119">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="2a1fa-120">要儲存之階層的根節點。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-120">Root node of the hierarchy to be saved.</span></span> <span data-ttu-id="2a1fa-121">請參閱 [**D3DXFRAME**](d3dxframe.md)。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-121">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a1fa-122">*pAnimController* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a1fa-122">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1fa-123">類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1fa-123">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="2a1fa-124">具有要儲存之動畫集的動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-124">Animation controller that has animation sets to be stored.</span></span> <span data-ttu-id="2a1fa-125">請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-125">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a1fa-126">*pUserDataSaver* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a1fa-126">*pUserDataSaver* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1fa-127">類型： **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1fa-127">Type: **[**LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span></span>

<span data-ttu-id="2a1fa-128">應用程式提供的介面，可儲存使用者資料。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-128">Application-provided interface that allows saving of user data.</span></span> <span data-ttu-id="2a1fa-129">請參閱 [**ID3DXSaveUserData**](id3dxsaveuserdata.md)。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-129">See [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a1fa-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a1fa-130">Return value</span></span>

<span data-ttu-id="2a1fa-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a1fa-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a1fa-132">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2a1fa-133">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-133">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a1fa-134">備註</span><span class="sxs-lookup"><span data-stu-id="2a1fa-134">Remarks</span></span>

<span data-ttu-id="2a1fa-135">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2a1fa-136">如果已定義 Unicode，函式呼叫會解析為 D3DXSaveMeshHierarchyToFileW。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-136">If Unicode is defined, the function call resolves to D3DXSaveMeshHierarchyToFileW.</span></span> <span data-ttu-id="2a1fa-137">否則，函式呼叫會解析為 D3DXSaveMeshHierarchyToFileA。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-137">Otherwise, the function call resolves to D3DXSaveMeshHierarchyToFileA.</span></span>

<span data-ttu-id="2a1fa-138">此函數不會儲存壓縮的動畫集。</span><span class="sxs-lookup"><span data-stu-id="2a1fa-138">This function does not save compressed animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a1fa-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a1fa-139">Requirements</span></span>



| <span data-ttu-id="2a1fa-140">需求</span><span class="sxs-lookup"><span data-stu-id="2a1fa-140">Requirement</span></span> | <span data-ttu-id="2a1fa-141">值</span><span class="sxs-lookup"><span data-stu-id="2a1fa-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1fa-142">標頭</span><span class="sxs-lookup"><span data-stu-id="2a1fa-142">Header</span></span><br/>  | <dl> <span data-ttu-id="2a1fa-143"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a1fa-143"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2a1fa-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a1fa-144">Library</span></span><br/> | <dl> <span data-ttu-id="2a1fa-145"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a1fa-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a1fa-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a1fa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1fa-147">動畫函數</span><span class="sxs-lookup"><span data-stu-id="2a1fa-147">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[<span data-ttu-id="2a1fa-148">X 檔案參考</span><span class="sxs-lookup"><span data-stu-id="2a1fa-148">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
