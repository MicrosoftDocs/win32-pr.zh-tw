---
description: ID3DXFileEnumObject：： System.windows.media.visualtreehelper.getchild 方法-抓取這個檔案資料物件中的子物件。
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'ID3DXFileEnumObject：： System.windows.media.visualtreehelper.getchild 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090356"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="c1a3d-103">ID3DXFileEnumObject：： System.windows.media.visualtreehelper.getchild 方法</span><span class="sxs-lookup"><span data-stu-id="c1a3d-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="c1a3d-104">抓取這個檔案資料物件中的子物件。</span><span class="sxs-lookup"><span data-stu-id="c1a3d-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a3d-105">語法</span><span class="sxs-lookup"><span data-stu-id="c1a3d-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="c1a3d-106">參數</span><span class="sxs-lookup"><span data-stu-id="c1a3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a3d-107"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="c1a3d-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a3d-108">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1a3d-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1a3d-109">要取出之子物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1a3d-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c1a3d-110">*ppObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1a3d-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a3d-111">類型： **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c1a3d-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="c1a3d-112">用來接收子物件介面指標之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c1a3d-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a3d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1a3d-113">Return value</span></span>

<span data-ttu-id="c1a3d-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1a3d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1a3d-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c1a3d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c1a3d-116">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE，D3DXFERR \_ NOMOREOBJECTS。</span><span class="sxs-lookup"><span data-stu-id="c1a3d-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a3d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1a3d-117">Requirements</span></span>



| <span data-ttu-id="c1a3d-118">需求</span><span class="sxs-lookup"><span data-stu-id="c1a3d-118">Requirement</span></span> | <span data-ttu-id="c1a3d-119">值</span><span class="sxs-lookup"><span data-stu-id="c1a3d-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a3d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c1a3d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c1a3d-121"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a3d-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c1a3d-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1a3d-122">Library</span></span><br/> | <dl> <span data-ttu-id="c1a3d-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1a3d-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c1a3d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1a3d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a3d-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="c1a3d-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
