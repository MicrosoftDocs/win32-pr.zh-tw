---
description: 捕獲二進位資料的大小。 已取代。
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'IDirectXFileBinary：： GetSize 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514661"
---
# <a name="idirectxfilebinarygetsize-method"></a><span data-ttu-id="56c1e-104">IDirectXFileBinary：： GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="56c1e-104">IDirectXFileBinary::GetSize method</span></span>

<span data-ttu-id="56c1e-105">捕獲二進位資料的大小。</span><span class="sxs-lookup"><span data-stu-id="56c1e-105">Retrieves the size of the binary data.</span></span> <span data-ttu-id="56c1e-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="56c1e-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c1e-107">語法</span><span class="sxs-lookup"><span data-stu-id="56c1e-107">Syntax</span></span>


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="56c1e-108">參數</span><span class="sxs-lookup"><span data-stu-id="56c1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c1e-109">*pcbSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56c1e-109">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56c1e-110">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="56c1e-110">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="56c1e-111">傳回之二進位資料大小的指標（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="56c1e-111">Pointer to the returned size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c1e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="56c1e-112">Return value</span></span>

<span data-ttu-id="56c1e-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56c1e-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56c1e-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="56c1e-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="56c1e-115">如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="56c1e-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c1e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="56c1e-116">Requirements</span></span>



| <span data-ttu-id="56c1e-117">需求</span><span class="sxs-lookup"><span data-stu-id="56c1e-117">Requirement</span></span> | <span data-ttu-id="56c1e-118">值</span><span class="sxs-lookup"><span data-stu-id="56c1e-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56c1e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="56c1e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="56c1e-120"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="56c1e-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="56c1e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="56c1e-121">Library</span></span><br/> | <dl> <span data-ttu-id="56c1e-122"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="56c1e-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c1e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56c1e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c1e-124">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="56c1e-124">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
