---
description: MergeBlob 函式會將來源 BLOB 中的所有專案複製到目的地 BLOB。
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: 'MergeBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943516"
---
# <a name="mergeblob-function"></a><span data-ttu-id="0d67d-103">MergeBlob 函式</span><span class="sxs-lookup"><span data-stu-id="0d67d-103">MergeBlob function</span></span>

<span data-ttu-id="0d67d-104">**MergeBlob** 函式會將來源 blob 中的所有專案複製到目的地 blob。</span><span class="sxs-lookup"><span data-stu-id="0d67d-104">The **MergeBlob** function copies all of the entries from the source BLOB into a destination BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d67d-105">語法</span><span class="sxs-lookup"><span data-stu-id="0d67d-105">Syntax</span></span>


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a><span data-ttu-id="0d67d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d67d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d67d-107">*hDstBlob* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0d67d-107">*hDstBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d67d-108">目的地 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d67d-108">Handle to the destination BLOB.</span></span> <span data-ttu-id="0d67d-109">在輸入時，此 BLOB 包含其原始資訊。</span><span class="sxs-lookup"><span data-stu-id="0d67d-109">On input, this BLOB contains its original information.</span></span> <span data-ttu-id="0d67d-110">在輸出中，此 BLOB 包含其原始資訊，以及來源 BLOB 的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="0d67d-110">On output, this BLOB contains its original information plus all the information of the source BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="0d67d-111">*hSrcBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d67d-111">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d67d-112">來源 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d67d-112">Handle to the source BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d67d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d67d-113">Return value</span></span>

<span data-ttu-id="0d67d-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="0d67d-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0d67d-115">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="0d67d-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d67d-116">備註</span><span class="sxs-lookup"><span data-stu-id="0d67d-116">Remarks</span></span>

<span data-ttu-id="0d67d-117">來源和目的地檔案的通用專案將會以來源 BLOB 的資料覆寫。</span><span class="sxs-lookup"><span data-stu-id="0d67d-117">Entries common to source and destination files will be overwritten with data from the source BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d67d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d67d-118">Requirements</span></span>



| <span data-ttu-id="0d67d-119">需求</span><span class="sxs-lookup"><span data-stu-id="0d67d-119">Requirement</span></span> | <span data-ttu-id="0d67d-120">值</span><span class="sxs-lookup"><span data-stu-id="0d67d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d67d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d67d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d67d-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d67d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0d67d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d67d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d67d-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d67d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d67d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="0d67d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d67d-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="0d67d-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="0d67d-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="0d67d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d67d-128"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d67d-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="0d67d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0d67d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d67d-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d67d-130"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




