---
description: 在給定 ID3DXFileEnumObject 列舉物件的情況下註冊自訂範本。
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile：： RegisterEnumTemplates 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386484"
---
# <a name="id3dxfileregisterenumtemplates-method"></a><span data-ttu-id="b1609-103">ID3DXFile：： RegisterEnumTemplates 方法</span><span class="sxs-lookup"><span data-stu-id="b1609-103">ID3DXFile::RegisterEnumTemplates method</span></span>

<span data-ttu-id="b1609-104">在給定 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 列舉物件的情況下註冊自訂範本。</span><span class="sxs-lookup"><span data-stu-id="b1609-104">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1609-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1609-105">Syntax</span></span>


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="b1609-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1609-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1609-107">*pEnum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1609-107">*pEnum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1609-108">類型： **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1609-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span></span>

<span data-ttu-id="b1609-109">包含範本之 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 列舉物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b1609-109">Pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object that contains templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1609-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1609-110">Return value</span></span>

<span data-ttu-id="b1609-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1609-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1609-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b1609-112">If the method succeeds, the return value is S\_OK .</span></span>

<span data-ttu-id="b1609-113">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="b1609-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1609-114">備註</span><span class="sxs-lookup"><span data-stu-id="b1609-114">Remarks</span></span>

<span data-ttu-id="b1609-115">當呼叫這個方法時，它會將以 ID3DXFileEnumObject 儲存的範本（代表檔案）複製到 [**ID3DXFile**](id3dxfile.md) 物件的本機範本存放區。</span><span class="sxs-lookup"><span data-stu-id="b1609-115">When this method is called, it copies templates stored with the ID3DXFileEnumObject, representing the file, to the local template store of the [**ID3DXFile**](id3dxfile.md) object.</span></span>

<span data-ttu-id="b1609-116">如果無法使用 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 指標，請改為呼叫 [**RegisterTemplates**](id3dxfile--registertemplates.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b1609-116">If an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pointer is not available, call the [**RegisterTemplates**](id3dxfile--registertemplates.md) method instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1609-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1609-117">Requirements</span></span>



| <span data-ttu-id="b1609-118">需求</span><span class="sxs-lookup"><span data-stu-id="b1609-118">Requirement</span></span> | <span data-ttu-id="b1609-119">值</span><span class="sxs-lookup"><span data-stu-id="b1609-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1609-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b1609-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b1609-121"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1609-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b1609-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1609-122">Library</span></span><br/> | <dl> <span data-ttu-id="b1609-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1609-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b1609-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1609-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1609-125">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="b1609-125">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="b1609-126">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="b1609-126">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




