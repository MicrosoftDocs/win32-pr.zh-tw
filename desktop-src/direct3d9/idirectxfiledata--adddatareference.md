---
description: 建立資料參考物件，並將其新增為子物件。 已取代。
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'IDirectXFileData：： AddDataReference 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982205"
---
# <a name="idirectxfiledataadddatareference-method"></a><span data-ttu-id="6833c-104">IDirectXFileData：： AddDataReference 方法</span><span class="sxs-lookup"><span data-stu-id="6833c-104">IDirectXFileData::AddDataReference method</span></span>

<span data-ttu-id="6833c-105">建立資料參考物件，並將其新增為子物件。</span><span class="sxs-lookup"><span data-stu-id="6833c-105">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="6833c-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="6833c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6833c-107">語法</span><span class="sxs-lookup"><span data-stu-id="6833c-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a><span data-ttu-id="6833c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6833c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6833c-109">*szRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6833c-109">*szRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6833c-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6833c-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6833c-111">參考之資料物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="6833c-111">Pointer to the name of the referenced data object.</span></span> <span data-ttu-id="6833c-112">如果 pguidRef 提供 GUID 的參考，則這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6833c-112">This parameter can be **NULL** if pguidRef provides a reference to the GUID.</span></span>

</dd> <dt>

<span data-ttu-id="6833c-113">*pguidRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6833c-113">*pguidRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6833c-114">類型： **Const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="6833c-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="6833c-115">代表資料之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="6833c-115">Pointer to the GUID representing the data.</span></span> <span data-ttu-id="6833c-116">如果 szRef 提供名稱的參考，則這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6833c-116">This parameter can be **NULL** if szRef provides a reference to the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6833c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6833c-117">Return value</span></span>

<span data-ttu-id="6833c-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6833c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6833c-119">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6833c-119">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="6833c-120">如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="6833c-120">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="6833c-121">備註</span><span class="sxs-lookup"><span data-stu-id="6833c-121">Remarks</span></span>

<span data-ttu-id="6833c-122">若要讓這個方法成功，szRef 或 pguidRef 參數都必須為非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6833c-122">For this method to succeed, either the szRef or pguidRef parameter must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6833c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6833c-123">Requirements</span></span>



| <span data-ttu-id="6833c-124">需求</span><span class="sxs-lookup"><span data-stu-id="6833c-124">Requirement</span></span> | <span data-ttu-id="6833c-125">值</span><span class="sxs-lookup"><span data-stu-id="6833c-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6833c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6833c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6833c-127"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="6833c-127"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="6833c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="6833c-128">Library</span></span><br/> | <dl> <span data-ttu-id="6833c-129"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6833c-129"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6833c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6833c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6833c-131">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="6833c-131">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 
