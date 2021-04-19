---
description: GetNPPEtypeSapFilter 函式會從指定的 BLOB 抓取 Etype/Sap 篩選器。
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: 'GetNPPEtypeSapFilter 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982115"
---
# <a name="getnppetypesapfilter-function"></a><span data-ttu-id="6c6a4-103">GetNPPEtypeSapFilter 函式</span><span class="sxs-lookup"><span data-stu-id="6c6a4-103">GetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="6c6a4-104">**GetNPPEtypeSapFilter** 函式會從指定的 BLOB 抓取 Etype/Sap 篩選器。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-104">The **GetNPPEtypeSapFilter** function retrieves the Etype/Sap filter from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c6a4-105">Syntax</span></span>


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6c6a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c6a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6a4-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a4-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a4-109">*pnSaps* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-109">*pnSaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a4-110">SAP 資料表中傳回的通訊協定數目指標。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-110">Pointer to the returned number of protocols in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a4-111">*pnEtypes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-111">*pnEtypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a4-112">在 Etype 資料表中傳回之 Etypes 數目的指標。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-112">Pointer to the returned number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a4-113">*ppSapTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-113">*ppSapTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a4-114">傳回的 SAP 資料表指標。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-114">Pointer to the returned SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a4-115">*ppEtypeTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-115">*ppEtypeTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a4-116">傳回之 Etype 資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-116">Pointer to the returned Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a4-117">*pFilterFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-117">*pFilterFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a4-118">傳回之篩選旗標的指標。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-118">Pointer to the returned filter flags.</span></span>

</dd> <dt>

<span data-ttu-id="6c6a4-119">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6a4-120">錯誤 BLOB 的控制碼，指定發生錯誤時，發生錯誤)  (原始 BLOB 中的位置。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-120">Handle to an error BLOB, which specifies the location in the original BLOB where the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6a4-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c6a4-121">Return value</span></span>

<span data-ttu-id="6c6a4-122">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6c6a4-123">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6a4-124">備註</span><span class="sxs-lookup"><span data-stu-id="6c6a4-124">Remarks</span></span>

<span data-ttu-id="6c6a4-125">Etype/Sap 資訊會儲存在 NPP **Owner** 區段的 **Config** 類別中。</span><span class="sxs-lookup"><span data-stu-id="6c6a4-125">The Etype/Sap information is stored in the **Config** category of the NPP **Owner** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6a4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c6a4-126">Requirements</span></span>



| <span data-ttu-id="6c6a4-127">需求</span><span class="sxs-lookup"><span data-stu-id="6c6a4-127">Requirement</span></span> | <span data-ttu-id="6c6a4-128">值</span><span class="sxs-lookup"><span data-stu-id="6c6a4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6a4-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c6a4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6a4-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6c6a4-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c6a4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6a4-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c6a4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c6a4-133">標頭</span><span class="sxs-lookup"><span data-stu-id="6c6a4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c6a4-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a4-134"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6c6a4-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c6a4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c6a4-136"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a4-136"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c6a4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6a4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c6a4-138"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a4-138"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c6a4-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c6a4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6a4-140">SetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="6c6a4-140">SetNPPEtypeSapFilter</span></span>](setnppetypesapfilter.md)
</dt> </dl>

 

 




