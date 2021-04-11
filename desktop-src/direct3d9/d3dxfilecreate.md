---
description: 建立 ID3DXFile 物件的實例。
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: 'D3DXFileCreate 函式 (D3DX9Xof) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116225"
---
# <a name="d3dxfilecreate-function"></a><span data-ttu-id="bc877-103">D3DXFileCreate 函式</span><span class="sxs-lookup"><span data-stu-id="bc877-103">D3DXFileCreate function</span></span>

<span data-ttu-id="bc877-104">建立 [**ID3DXFile**](id3dxfile.md) 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="bc877-104">Creates an instance of an [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc877-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc877-105">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="bc877-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc877-107">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="bc877-107">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="bc877-108">類型： **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bc877-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="bc877-109">[**ID3DXFile**](id3dxfile.md)介面指標的位址，表示已建立的. x 檔案物件。</span><span class="sxs-lookup"><span data-stu-id="bc877-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the created .x file object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc877-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc877-110">Return value</span></span>

<span data-ttu-id="bc877-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc877-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc877-112">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="bc877-112">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc877-113">如果函式失敗，則傳回值可以是下列其中一項： E \_ 指標、e \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="bc877-113">If the function fails, the return value can be one of the following: E\_POINTER, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc877-114">備註</span><span class="sxs-lookup"><span data-stu-id="bc877-114">Remarks</span></span>

<span data-ttu-id="bc877-115">使用這個函數之後，請使用 [**RegisterTemplates**](id3dxfile--registertemplates.md) 或 [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) 來註冊範本、建立 [**CreateEnumObject**](id3dxfile--createenumobject.md) 來建立列舉值物件，或使用 [**CreateSaveObject**](id3dxfile--createsaveobject.md) 來建立儲存物件。</span><span class="sxs-lookup"><span data-stu-id="bc877-115">After using this function, use [**RegisterTemplates**](id3dxfile--registertemplates.md) or [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) to register templates, [**CreateEnumObject**](id3dxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](id3dxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc877-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc877-116">Requirements</span></span>



| <span data-ttu-id="bc877-117">需求</span><span class="sxs-lookup"><span data-stu-id="bc877-117">Requirement</span></span> | <span data-ttu-id="bc877-118">值</span><span class="sxs-lookup"><span data-stu-id="bc877-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc877-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bc877-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bc877-120"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc877-120"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="bc877-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc877-121">Library</span></span><br/> | <dl> <span data-ttu-id="bc877-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc877-122"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bc877-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc877-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc877-124">D3DX X 檔案函數</span><span class="sxs-lookup"><span data-stu-id="bc877-124">D3DX X File Functions</span></span>](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="bc877-125">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="bc877-125">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="bc877-126">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="bc877-126">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="bc877-127">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="bc877-127">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[<span data-ttu-id="bc877-128">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="bc877-128">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




