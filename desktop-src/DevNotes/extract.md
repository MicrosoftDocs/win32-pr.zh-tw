---
description: 解壓縮函數會從封包中解壓縮檔案。
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: 擷取函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001596"
---
# <a name="extract-function"></a><span data-ttu-id="2ba63-103">擷取函式</span><span class="sxs-lookup"><span data-stu-id="2ba63-103">Extract function</span></span>

<span data-ttu-id="2ba63-104">\[不再支援此函式，因此無法保證其行為。\]</span><span class="sxs-lookup"><span data-stu-id="2ba63-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="2ba63-105">**解壓縮** 函數會從封包中解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="2ba63-105">The **Extract** function extracts files from a cabinet.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba63-106">語法</span><span class="sxs-lookup"><span data-stu-id="2ba63-106">Syntax</span></span>


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a><span data-ttu-id="2ba63-107">參數</span><span class="sxs-lookup"><span data-stu-id="2ba63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba63-108">*Ps*</span><span class="sxs-lookup"><span data-stu-id="2ba63-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="2ba63-109">[**會話**](session.md)結構的指標，其中包含目前會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2ba63-109">Pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

</dd> <dt>

<span data-ttu-id="2ba63-110">*lpCabName*</span><span class="sxs-lookup"><span data-stu-id="2ba63-110">*lpCabName*</span></span> 
</dt> <dd>

<span data-ttu-id="2ba63-111">要從中解壓縮檔案的封包名稱指標。</span><span class="sxs-lookup"><span data-stu-id="2ba63-111">Pointer to the name of the cabinet from which files are to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ba63-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ba63-112">Return value</span></span>

<span data-ttu-id="2ba63-113">如果函式成功，則會傳回 **S \_ OK**，否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2ba63-113">If the function succeeds, it returns **S\_OK**; otherwise, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ba63-114">備註</span><span class="sxs-lookup"><span data-stu-id="2ba63-114">Remarks</span></span>

<span data-ttu-id="2ba63-115">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="2ba63-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba63-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ba63-116">Requirements</span></span>



| <span data-ttu-id="2ba63-117">需求</span><span class="sxs-lookup"><span data-stu-id="2ba63-117">Requirement</span></span> | <span data-ttu-id="2ba63-118">值</span><span class="sxs-lookup"><span data-stu-id="2ba63-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba63-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2ba63-119">DLL</span></span><br/> | <dl> <span data-ttu-id="2ba63-120"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ba63-120"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba63-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ba63-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba63-122">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="2ba63-122">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="2ba63-123">**ERF**</span><span class="sxs-lookup"><span data-stu-id="2ba63-123">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[<span data-ttu-id="2ba63-124">**會話**</span><span class="sxs-lookup"><span data-stu-id="2ba63-124">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
