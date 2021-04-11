---
description: 抓取多用途網際網路郵件延伸 (MIME) 類型的二進位資料。 已取代。
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'IDirectXFileBinary：： GetMimeType 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946084"
---
# <a name="idirectxfilebinarygetmimetype-method"></a><span data-ttu-id="936db-104">IDirectXFileBinary：： GetMimeType 方法</span><span class="sxs-lookup"><span data-stu-id="936db-104">IDirectXFileBinary::GetMimeType method</span></span>

<span data-ttu-id="936db-105">抓取多用途網際網路郵件延伸 (MIME) 類型的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="936db-105">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="936db-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="936db-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="936db-107">語法</span><span class="sxs-lookup"><span data-stu-id="936db-107">Syntax</span></span>


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a><span data-ttu-id="936db-108">參數</span><span class="sxs-lookup"><span data-stu-id="936db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936db-109">*pszMimeType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="936db-109">*pszMimeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="936db-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="936db-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="936db-111">要接收 MIME 類型字串之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="936db-111">Address of a pointer to receive the MIME type string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936db-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="936db-112">Return value</span></span>

<span data-ttu-id="936db-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="936db-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="936db-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="936db-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="936db-115">如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="936db-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="936db-116">備註</span><span class="sxs-lookup"><span data-stu-id="936db-116">Remarks</span></span>

<span data-ttu-id="936db-117">當二進位物件的 DirectX 檔案中未指定 MIME 類型時，此函式會將 pszMimeType 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="936db-117">When there is no MIME type specified in a DirectX file for a binary object, the function will set pszMimeType to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="936db-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="936db-118">Requirements</span></span>



| <span data-ttu-id="936db-119">需求</span><span class="sxs-lookup"><span data-stu-id="936db-119">Requirement</span></span> | <span data-ttu-id="936db-120">值</span><span class="sxs-lookup"><span data-stu-id="936db-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="936db-121">標頭</span><span class="sxs-lookup"><span data-stu-id="936db-121">Header</span></span><br/>  | <dl> <span data-ttu-id="936db-122"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="936db-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="936db-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="936db-123">Library</span></span><br/> | <dl> <span data-ttu-id="936db-124"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="936db-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936db-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="936db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936db-126">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="936db-126">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
