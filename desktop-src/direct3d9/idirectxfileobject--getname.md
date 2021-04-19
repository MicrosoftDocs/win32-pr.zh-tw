---
description: 捕獲 DirectX 檔案物件名稱的指標。 已取代。
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'IDirectXFileObject：： GetName 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979873"
---
# <a name="idirectxfileobjectgetname-method"></a><span data-ttu-id="54b76-104">IDirectXFileObject：： GetName 方法</span><span class="sxs-lookup"><span data-stu-id="54b76-104">IDirectXFileObject::GetName method</span></span>

<span data-ttu-id="54b76-105">捕獲 DirectX 檔案物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="54b76-105">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="54b76-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="54b76-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b76-107">語法</span><span class="sxs-lookup"><span data-stu-id="54b76-107">Syntax</span></span>


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="54b76-108">參數</span><span class="sxs-lookup"><span data-stu-id="54b76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b76-109">*pstrNameBuf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="54b76-109">*pstrNameBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b76-110">類型： **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b76-110">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b76-111">緩衝區的指標，其中將複製 DirectX 檔案物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="54b76-111">Pointer to the buffer in which the DirectX file object's name will be copied.</span></span> <span data-ttu-id="54b76-112">如果只需要緩衝區長度，則設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="54b76-112">Set to **NULL** if only the buffer length is needed.</span></span>

</dd> <dt>

<span data-ttu-id="54b76-113">*pdwBufLen* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="54b76-113">*pdwBufLen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b76-114">類型： **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b76-114">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b76-115">DWORD 的指標，指定 pstrNameBuf 所指向的緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="54b76-115">Pointer to a DWORD specifying the length of the buffer pointed to by pstrNameBuf.</span></span> <span data-ttu-id="54b76-116">即使 pstrNameBuf 為 **Null**，pdwBufLen 參數值仍會修改為保留物件名稱所需的緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="54b76-116">The pdwBufLen parameter value will be modified to the buffer length needed to hold the object's name even if pstrNameBuf is **NULL**.</span></span> <span data-ttu-id="54b76-117">無論是哪一種情況， \_ 如果 pdwBufLen 的原始值不等於或大於保留物件名稱所需的長度，函數都會傳回 DXFILEERR BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="54b76-117">In either case, the function will return DXFILEERR\_BADVALUE if the original value of pdwBufLen is not as large as or larger than the length needed to hold the object's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b76-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="54b76-118">Return value</span></span>

<span data-ttu-id="54b76-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54b76-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54b76-120">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="54b76-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="54b76-121">如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="54b76-121">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="54b76-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="54b76-122">Requirements</span></span>



| <span data-ttu-id="54b76-123">需求</span><span class="sxs-lookup"><span data-stu-id="54b76-123">Requirement</span></span> | <span data-ttu-id="54b76-124">值</span><span class="sxs-lookup"><span data-stu-id="54b76-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54b76-125">標頭</span><span class="sxs-lookup"><span data-stu-id="54b76-125">Header</span></span><br/>  | <dl> <span data-ttu-id="54b76-126"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="54b76-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="54b76-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="54b76-127">Library</span></span><br/> | <dl> <span data-ttu-id="54b76-128"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="54b76-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54b76-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54b76-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b76-130">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="54b76-130">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 
