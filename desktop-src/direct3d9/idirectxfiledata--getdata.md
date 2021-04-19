---
description: 抓取其中一個物件成員的資料，或所有成員的資料。 已取代。
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'IDirectXFileData：： DXFile 方法 (.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977137"
---
# <a name="idirectxfiledatagetdata-method"></a><span data-ttu-id="46e5f-104">IDirectXFileData：：：：的方法</span><span class="sxs-lookup"><span data-stu-id="46e5f-104">IDirectXFileData::GetData method</span></span>

<span data-ttu-id="46e5f-105">抓取其中一個物件成員的資料，或所有成員的資料。</span><span class="sxs-lookup"><span data-stu-id="46e5f-105">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="46e5f-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="46e5f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e5f-107">語法</span><span class="sxs-lookup"><span data-stu-id="46e5f-107">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a><span data-ttu-id="46e5f-108">參數</span><span class="sxs-lookup"><span data-stu-id="46e5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e5f-109">*szMember* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e5f-109">*szMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e5f-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46e5f-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46e5f-111">要取得其資料之成員名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="46e5f-111">Pointer to the name of the member for which to retrieve data.</span></span> <span data-ttu-id="46e5f-112">指定 **Null** 以抓取所有必要的成員資料。</span><span class="sxs-lookup"><span data-stu-id="46e5f-112">Specify **NULL** to retrieve all required members' data.</span></span>

</dd> <dt>

<span data-ttu-id="46e5f-113">*pcbSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46e5f-113">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e5f-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="46e5f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46e5f-115">接收 ppvData 緩衝區大小的指標（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="46e5f-115">Pointer to receive the ppvData buffer size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="46e5f-116">*ppvData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46e5f-116">*ppvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e5f-117">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="46e5f-117">Type: **void\*\***</span></span>

<span data-ttu-id="46e5f-118">緩衝區指標的位址，用來接收與 szMember 相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="46e5f-118">Address of a pointer to the buffer to receive the data associated with szMember.</span></span> <span data-ttu-id="46e5f-119">如果 szMember 為 **Null**，則 ppvData 會設定為指向在連續記憶體區塊中包含所有必要成員資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="46e5f-119">If szMember is **NULL**, ppvData is set to point to a buffer containing all required members' data in a contiguous block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e5f-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="46e5f-120">Return value</span></span>

<span data-ttu-id="46e5f-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46e5f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46e5f-122">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="46e5f-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="46e5f-123">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADARRAYSIZE、DXFILEERR \_ BADDATAREFERENCE、DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="46e5f-123">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADDataReference, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e5f-124">備註</span><span class="sxs-lookup"><span data-stu-id="46e5f-124">Remarks</span></span>

<span data-ttu-id="46e5f-125">這個方法會抓取資料物件所需成員的資料，但不會取得選擇性 (子) 成員的資料。</span><span class="sxs-lookup"><span data-stu-id="46e5f-125">This method retrieves the data for required members of a data object but no data for optional (child) members.</span></span> <span data-ttu-id="46e5f-126">使用 [**IDirectXFileData：： GetNextObject**](idirectxfiledata--getnextobject.md) 來取出子物件。</span><span class="sxs-lookup"><span data-stu-id="46e5f-126">Use [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) to retrieve child objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e5f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="46e5f-127">Requirements</span></span>



| <span data-ttu-id="46e5f-128">需求</span><span class="sxs-lookup"><span data-stu-id="46e5f-128">Requirement</span></span> | <span data-ttu-id="46e5f-129">值</span><span class="sxs-lookup"><span data-stu-id="46e5f-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46e5f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="46e5f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="46e5f-131"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="46e5f-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="46e5f-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="46e5f-132">Library</span></span><br/> | <dl> <span data-ttu-id="46e5f-133"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="46e5f-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e5f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46e5f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e5f-135">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="46e5f-135">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="46e5f-136">**IDirectXFileData::GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="46e5f-136">**IDirectXFileData::GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
