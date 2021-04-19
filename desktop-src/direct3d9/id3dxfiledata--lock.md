---
description: 存取. x 檔案資料。
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData：： Lock 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974871"
---
# <a name="id3dxfiledatalock-method"></a><span data-ttu-id="472b1-103">ID3DXFileData：： Lock 方法</span><span class="sxs-lookup"><span data-stu-id="472b1-103">ID3DXFileData::Lock method</span></span>

<span data-ttu-id="472b1-104">存取. x 檔案資料。</span><span class="sxs-lookup"><span data-stu-id="472b1-104">Accesses the .x file data.</span></span>

## <a name="syntax"></a><span data-ttu-id="472b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="472b1-105">Syntax</span></span>


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="472b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="472b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472b1-107">*pSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="472b1-107">*pSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="472b1-108">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="472b1-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="472b1-109">. X 檔案資料大小的指標。</span><span class="sxs-lookup"><span data-stu-id="472b1-109">Pointer to the size of the .x file data.</span></span>

</dd> <dt>

<span data-ttu-id="472b1-110">*ppData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="472b1-110">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="472b1-111">類型： **CONST VOID \* \***</span><span class="sxs-lookup"><span data-stu-id="472b1-111">Type: **const VOID\*\***</span></span>

<span data-ttu-id="472b1-112">接收 [**ID3DXFileData**](id3dxfiledata.md) 檔案資料物件介面指標的指標位址。</span><span class="sxs-lookup"><span data-stu-id="472b1-112">Address of a pointer to receive the [**ID3DXFileData**](id3dxfiledata.md) file data object's interface pointer.</span></span> <span data-ttu-id="472b1-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="472b1-113">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472b1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="472b1-114">Return value</span></span>

<span data-ttu-id="472b1-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="472b1-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="472b1-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="472b1-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="472b1-117">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="472b1-117">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="472b1-118">備註</span><span class="sxs-lookup"><span data-stu-id="472b1-118">Remarks</span></span>

<span data-ttu-id="472b1-119">*PpData* 指標只在 **ID3DXFileData：： Lock** 期間有效 [**ID3DXFileData：： Unlock**](id3dxfiledata--unlock.md) sequence。</span><span class="sxs-lookup"><span data-stu-id="472b1-119">The *ppData* pointer is only valid during a **ID3DXFileData::Lock** ... [**ID3DXFileData::Unlock**](id3dxfiledata--unlock.md) sequence.</span></span> <span data-ttu-id="472b1-120">您可以進行多個鎖定呼叫。</span><span class="sxs-lookup"><span data-stu-id="472b1-120">You can make multiple lock calls.</span></span> <span data-ttu-id="472b1-121">不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。</span><span class="sxs-lookup"><span data-stu-id="472b1-121">However, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="472b1-122">由於檔案資料不保證會與位元組界限適當地對齊，因此您應該使用未對齊的指標來存取 *ppData* 。</span><span class="sxs-lookup"><span data-stu-id="472b1-122">Because file data is not guaranteed to be aligned properly with byte boundaries, you should access *ppData* with UNALIGNED pointers.</span></span>

<span data-ttu-id="472b1-123">傳回的參數值因為可能的檔案損毀而無法保證有效;因此，您的程式碼應該會驗證傳回的參數值。</span><span class="sxs-lookup"><span data-stu-id="472b1-123">Returned parameter values are not guaranteed to be valid due to possible file corruption; therefore, your code should verify the returned parameter values.</span></span>

## <a name="requirements"></a><span data-ttu-id="472b1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="472b1-124">Requirements</span></span>



| <span data-ttu-id="472b1-125">需求</span><span class="sxs-lookup"><span data-stu-id="472b1-125">Requirement</span></span> | <span data-ttu-id="472b1-126">值</span><span class="sxs-lookup"><span data-stu-id="472b1-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="472b1-127">標頭</span><span class="sxs-lookup"><span data-stu-id="472b1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="472b1-128"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="472b1-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="472b1-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="472b1-129">Library</span></span><br/> | <dl> <span data-ttu-id="472b1-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="472b1-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="472b1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="472b1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472b1-132">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="472b1-132">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
