---
description: 讀取二進位資料。 已取代。
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'IDirectXFileBinary：： Read 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035400"
---
# <a name="idirectxfilebinaryread-method"></a><span data-ttu-id="a85e3-104">IDirectXFileBinary：： Read 方法</span><span class="sxs-lookup"><span data-stu-id="a85e3-104">IDirectXFileBinary::Read method</span></span>

<span data-ttu-id="a85e3-105">讀取二進位資料。</span><span class="sxs-lookup"><span data-stu-id="a85e3-105">Reads the binary data.</span></span> <span data-ttu-id="a85e3-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="a85e3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a85e3-107">語法</span><span class="sxs-lookup"><span data-stu-id="a85e3-107">Syntax</span></span>


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="a85e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="a85e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a85e3-109">*pvData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a85e3-109">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a85e3-110">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a85e3-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a85e3-111">接收已讀取資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="a85e3-111">Pointer to the buffer that receives the data that has been read.</span></span>

</dd> <dt>

<span data-ttu-id="a85e3-112">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a85e3-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a85e3-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a85e3-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a85e3-114">PvData 所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a85e3-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a85e3-115">*pcbRead* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a85e3-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a85e3-116">類型： **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a85e3-116">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a85e3-117">實際讀取的位元組數目的指標。</span><span class="sxs-lookup"><span data-stu-id="a85e3-117">Pointer to the number of bytes actually read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a85e3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="a85e3-118">Return value</span></span>

<span data-ttu-id="a85e3-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a85e3-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a85e3-120">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a85e3-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="a85e3-121">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOMOREDATA。</span><span class="sxs-lookup"><span data-stu-id="a85e3-121">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="a85e3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a85e3-122">Requirements</span></span>



| <span data-ttu-id="a85e3-123">需求</span><span class="sxs-lookup"><span data-stu-id="a85e3-123">Requirement</span></span> | <span data-ttu-id="a85e3-124">值</span><span class="sxs-lookup"><span data-stu-id="a85e3-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a85e3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a85e3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a85e3-126"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="a85e3-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="a85e3-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="a85e3-127">Library</span></span><br/> | <dl> <span data-ttu-id="a85e3-128"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a85e3-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a85e3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a85e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85e3-130">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="a85e3-130">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
