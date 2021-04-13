---
description: 取得建立這個 ID3DXFileSaveObject 物件之物件的 ID3DXFile 介面。
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'ID3DXFileSaveObject：： GetFile 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386482"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a><span data-ttu-id="a83f6-103">ID3DXFileSaveObject：： GetFile 方法</span><span class="sxs-lookup"><span data-stu-id="a83f6-103">ID3DXFileSaveObject::GetFile method</span></span>

<span data-ttu-id="a83f6-104">取得建立這個 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md)物件之物件的 [**ID3DXFile**](id3dxfile.md)介面。</span><span class="sxs-lookup"><span data-stu-id="a83f6-104">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a83f6-105">語法</span><span class="sxs-lookup"><span data-stu-id="a83f6-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="a83f6-106">參數</span><span class="sxs-lookup"><span data-stu-id="a83f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a83f6-107">*ppFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a83f6-107">*ppFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a83f6-108">類型： **[ **ID3DXFile**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="a83f6-108">Type: **[**ID3DXFile**](id3dxfile.md)**</span></span>

<span data-ttu-id="a83f6-109">[**ID3DXFile**](id3dxfile.md)物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="a83f6-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a83f6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a83f6-110">Return value</span></span>

<span data-ttu-id="a83f6-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a83f6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a83f6-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a83f6-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a83f6-113">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE、e \_ NOINTERFACE、e \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="a83f6-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, E\_NOINTERFACE, E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="a83f6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a83f6-114">Requirements</span></span>



| <span data-ttu-id="a83f6-115">需求</span><span class="sxs-lookup"><span data-stu-id="a83f6-115">Requirement</span></span> | <span data-ttu-id="a83f6-116">值</span><span class="sxs-lookup"><span data-stu-id="a83f6-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a83f6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a83f6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a83f6-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="a83f6-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a83f6-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a83f6-119">Library</span></span><br/> | <dl> <span data-ttu-id="a83f6-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a83f6-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a83f6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a83f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83f6-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="a83f6-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




