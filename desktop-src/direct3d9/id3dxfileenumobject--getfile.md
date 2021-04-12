---
description: 抓取 ID3DXFile 物件。
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'ID3DXFileEnumObject：： GetFile 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946154"
---
# <a name="id3dxfileenumobjectgetfile-method"></a><span data-ttu-id="632cb-103">ID3DXFileEnumObject：： GetFile 方法</span><span class="sxs-lookup"><span data-stu-id="632cb-103">ID3DXFileEnumObject::GetFile method</span></span>

<span data-ttu-id="632cb-104">抓取 [**ID3DXFile**](id3dxfile.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="632cb-104">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="632cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="632cb-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="632cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="632cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="632cb-107">*ppFile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="632cb-107">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="632cb-108">類型： **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="632cb-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="632cb-109">[**ID3DXFile**](id3dxfile.md)介面指標的位址，表示傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="632cb-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the returned object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="632cb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="632cb-110">Return value</span></span>

<span data-ttu-id="632cb-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="632cb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="632cb-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="632cb-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="632cb-113">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="632cb-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="632cb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="632cb-114">Requirements</span></span>



| <span data-ttu-id="632cb-115">需求</span><span class="sxs-lookup"><span data-stu-id="632cb-115">Requirement</span></span> | <span data-ttu-id="632cb-116">值</span><span class="sxs-lookup"><span data-stu-id="632cb-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="632cb-117">標頭</span><span class="sxs-lookup"><span data-stu-id="632cb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="632cb-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="632cb-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="632cb-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="632cb-119">Library</span></span><br/> | <dl> <span data-ttu-id="632cb-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="632cb-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="632cb-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="632cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632cb-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="632cb-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 




