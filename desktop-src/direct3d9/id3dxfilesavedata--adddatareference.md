---
description: 將資料參考加入為這個 ID3DXFileSaveData 檔資料節點的子系。 資料參考會指向檔案資料物件。
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'ID3DXFileSaveData：： AddDataReference 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946152"
---
# <a name="id3dxfilesavedataadddatareference-method"></a><span data-ttu-id="2d603-104">ID3DXFileSaveData：： AddDataReference 方法</span><span class="sxs-lookup"><span data-stu-id="2d603-104">ID3DXFileSaveData::AddDataReference method</span></span>

<span data-ttu-id="2d603-105">將資料參考加入為這個 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 檔資料節點的子系。</span><span class="sxs-lookup"><span data-stu-id="2d603-105">Adds a data reference as a child of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span> <span data-ttu-id="2d603-106">資料參考會指向檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="2d603-106">The data reference points to a file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d603-107">語法</span><span class="sxs-lookup"><span data-stu-id="2d603-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a><span data-ttu-id="2d603-108">參數</span><span class="sxs-lookup"><span data-stu-id="2d603-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d603-109">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d603-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d603-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d603-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d603-111">要以傳址方式加入之資料物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="2d603-111">Pointer to the name of the data object to add by reference.</span></span> <span data-ttu-id="2d603-112">如果資料物件沒有名稱，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2d603-112">Specify **NULL** if the data object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="2d603-113">*pId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d603-113">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d603-114">類型： **Const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d603-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="2d603-115">GUID 的指標，代表要以傳址方式加入的資料物件。</span><span class="sxs-lookup"><span data-stu-id="2d603-115">Pointer to a GUID representing the data object to add by reference.</span></span> <span data-ttu-id="2d603-116">如果是 **Null**，將會加入參考，指向資料物件，並以 >szname 指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d603-116">If **NULL**, a reference will be added that points to the data object with the name given by szName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d603-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d603-117">Return value</span></span>

<span data-ttu-id="2d603-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d603-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d603-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2d603-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2d603-120">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADOBJECT、D3DXFERR \_ BADVALUE、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2d603-120">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d603-121">備註</span><span class="sxs-lookup"><span data-stu-id="2d603-121">Remarks</span></span>

<span data-ttu-id="2d603-122">所參考的檔案資料物件必須有名稱或 GUID。</span><span class="sxs-lookup"><span data-stu-id="2d603-122">The file data object being referenced must have either a name or a GUID.</span></span> <span data-ttu-id="2d603-123">File 資料物件也必須衍生自不同的父 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d603-123">The file data object must also derive from a different parent [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d603-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d603-124">Requirements</span></span>



| <span data-ttu-id="2d603-125">需求</span><span class="sxs-lookup"><span data-stu-id="2d603-125">Requirement</span></span> | <span data-ttu-id="2d603-126">值</span><span class="sxs-lookup"><span data-stu-id="2d603-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d603-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2d603-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2d603-128"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d603-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="2d603-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d603-129">Library</span></span><br/> | <dl> <span data-ttu-id="2d603-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d603-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d603-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d603-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d603-132">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="2d603-132">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
