---
description: 抓取具有指定名稱的資料物件。
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject：： GetDataObjectByName 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982891"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="81ffa-103">ID3DXFileEnumObject：： GetDataObjectByName 方法</span><span class="sxs-lookup"><span data-stu-id="81ffa-103">ID3DXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="81ffa-104">抓取具有指定名稱的資料物件。</span><span class="sxs-lookup"><span data-stu-id="81ffa-104">Retrieves the data object that has the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ffa-105">語法</span><span class="sxs-lookup"><span data-stu-id="81ffa-105">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="81ffa-106">參數</span><span class="sxs-lookup"><span data-stu-id="81ffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ffa-107">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81ffa-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ffa-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81ffa-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81ffa-109">所要求名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="81ffa-109">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="81ffa-110">*ppObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81ffa-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81ffa-111">類型： **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="81ffa-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="81ffa-112">[**ID3DXFileData**](id3dxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="81ffa-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ffa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="81ffa-113">Return value</span></span>

<span data-ttu-id="81ffa-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81ffa-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81ffa-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="81ffa-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="81ffa-116">如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="81ffa-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ffa-117">備註</span><span class="sxs-lookup"><span data-stu-id="81ffa-117">Remarks</span></span>

<span data-ttu-id="81ffa-118">使用 [**ID3DXFileData：： GetName**](id3dxfiledata--getname.md) 方法，取得目前檔案資料物件的名稱 >szname。</span><span class="sxs-lookup"><span data-stu-id="81ffa-118">Obtain the name szName of the current file data object with the [**ID3DXFileData::GetName**](id3dxfiledata--getname.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ffa-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="81ffa-119">Requirements</span></span>



| <span data-ttu-id="81ffa-120">需求</span><span class="sxs-lookup"><span data-stu-id="81ffa-120">Requirement</span></span> | <span data-ttu-id="81ffa-121">值</span><span class="sxs-lookup"><span data-stu-id="81ffa-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81ffa-122">標頭</span><span class="sxs-lookup"><span data-stu-id="81ffa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="81ffa-123"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="81ffa-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="81ffa-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="81ffa-124">Library</span></span><br/> | <dl> <span data-ttu-id="81ffa-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="81ffa-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="81ffa-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81ffa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ffa-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="81ffa-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
