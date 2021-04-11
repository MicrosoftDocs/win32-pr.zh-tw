---
description: 設定 BLOB Etype/Sap 篩選器。
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: 'SetNPPEtypeSapFilter 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318960"
---
# <a name="setnppetypesapfilter-function"></a><span data-ttu-id="3423e-103">SetNPPEtypeSapFilter 函式</span><span class="sxs-lookup"><span data-stu-id="3423e-103">SetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="3423e-104">**SetNPPEtypeSapFilter** 函數會設定 BLOB Etype/Sap 篩選器。</span><span class="sxs-lookup"><span data-stu-id="3423e-104">The **SetNPPEtypeSapFilter** function sets the BLOB Etype/Sap filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3423e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3423e-105">Syntax</span></span>


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3423e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3423e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3423e-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3423e-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3423e-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3423e-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3423e-109">*nSaps* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3423e-109">*nSaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3423e-110">Sap 的數目。</span><span class="sxs-lookup"><span data-stu-id="3423e-110">The number of SAPs.</span></span>

</dd> <dt>

<span data-ttu-id="3423e-111">*nEtypes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3423e-111">*nEtypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3423e-112">要設定之 Etype 資料表中的 Etypes 數目。</span><span class="sxs-lookup"><span data-stu-id="3423e-112">The number of Etypes in the Etype table being set.</span></span>

</dd> <dt>

<span data-ttu-id="3423e-113">*lpSapTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3423e-113">*lpSapTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3423e-114">已設定的 SAP 資料表指標。</span><span class="sxs-lookup"><span data-stu-id="3423e-114">A pointer to the SAP table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="3423e-115">*lpEtypeTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3423e-115">*lpEtypeTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3423e-116">已設定之 Etype 資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="3423e-116">A pointer to the Etype table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="3423e-117">*FilterFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3423e-117">*FilterFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3423e-118">已設定的篩選旗標。</span><span class="sxs-lookup"><span data-stu-id="3423e-118">The filter flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="3423e-119">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3423e-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3423e-120">錯誤 BLOB 的控制碼，指定當發生任何) 時，原始 BLOB 中的錯誤 (。</span><span class="sxs-lookup"><span data-stu-id="3423e-120">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3423e-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="3423e-121">Return value</span></span>

<span data-ttu-id="3423e-122">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="3423e-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3423e-123">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="3423e-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3423e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3423e-124">Requirements</span></span>



| <span data-ttu-id="3423e-125">需求</span><span class="sxs-lookup"><span data-stu-id="3423e-125">Requirement</span></span> | <span data-ttu-id="3423e-126">值</span><span class="sxs-lookup"><span data-stu-id="3423e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3423e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3423e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3423e-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3423e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3423e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3423e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3423e-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3423e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3423e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3423e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3423e-132"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3423e-132"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3423e-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="3423e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="3423e-134"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3423e-134"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3423e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3423e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3423e-136"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3423e-136"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3423e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3423e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3423e-138">GetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="3423e-138">GetNPPEtypeSapFilter</span></span>](getnppetypesapfilter.md)
</dt> </dl>

 

 




