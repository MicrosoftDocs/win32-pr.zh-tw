---
description: 註冊自訂範本。
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'ID3DXFile：： RegisterTemplates 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975689"
---
# <a name="id3dxfileregistertemplates-method"></a><span data-ttu-id="d85a1-103">ID3DXFile：： RegisterTemplates 方法</span><span class="sxs-lookup"><span data-stu-id="d85a1-103">ID3DXFile::RegisterTemplates method</span></span>

<span data-ttu-id="d85a1-104">註冊自訂範本。</span><span class="sxs-lookup"><span data-stu-id="d85a1-104">Registers custom templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="d85a1-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="d85a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="d85a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d85a1-107">*pvData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d85a1-107">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d85a1-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d85a1-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d85a1-109">緩衝區的指標，此緩衝區是由包含範本的文字或二進位格式的. x 檔案所組成。</span><span class="sxs-lookup"><span data-stu-id="d85a1-109">Pointer to a buffer consisting of a .x file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="d85a1-110">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d85a1-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d85a1-111">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d85a1-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d85a1-112">PvData 所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d85a1-112">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d85a1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d85a1-113">Return value</span></span>

<span data-ttu-id="d85a1-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d85a1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d85a1-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d85a1-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d85a1-116">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE，D3DXFERR \_ PARSEERROR。</span><span class="sxs-lookup"><span data-stu-id="d85a1-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d85a1-117">備註</span><span class="sxs-lookup"><span data-stu-id="d85a1-117">Remarks</span></span>

<span data-ttu-id="d85a1-118">下列程式碼片段提供 **RegisterTemplates** 的範例呼叫，以及 **pvData** 所指向之緩衝區的範例內容。</span><span class="sxs-lookup"><span data-stu-id="d85a1-118">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which **pvData** points.</span></span>


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



<span data-ttu-id="d85a1-119">所有範本都必須指定名稱和 UUID。</span><span class="sxs-lookup"><span data-stu-id="d85a1-119">All templates must specify a name and a UUID.</span></span>

<span data-ttu-id="d85a1-120">這個方法會呼叫 [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)方法，藉由呼叫 [**CreateEnumObject**](id3dxfile--createenumobject.md)和 **pvData** 做為第一個參數來取得 [**ID3DXFileEnumObject**](id3dxfileenumobject.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="d85a1-120">This method calls the [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) method, obtaining an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface pointer by calling [**CreateEnumObject**](id3dxfile--createenumobject.md) with **pvData** as the first parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d85a1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d85a1-121">Requirements</span></span>



| <span data-ttu-id="d85a1-122">需求</span><span class="sxs-lookup"><span data-stu-id="d85a1-122">Requirement</span></span> | <span data-ttu-id="d85a1-123">值</span><span class="sxs-lookup"><span data-stu-id="d85a1-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d85a1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d85a1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d85a1-125"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="d85a1-125"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d85a1-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d85a1-126">Library</span></span><br/> | <dl> <span data-ttu-id="d85a1-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d85a1-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d85a1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d85a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85a1-129">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="d85a1-129">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="d85a1-130">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="d85a1-130">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
