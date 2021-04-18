---
description: DuplicateBlob 函式會複製特定的 BLOB。
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: 'DuplicateBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971507"
---
# <a name="duplicateblob-function"></a><span data-ttu-id="66ed5-103">DuplicateBlob 函式</span><span class="sxs-lookup"><span data-stu-id="66ed5-103">DuplicateBlob function</span></span>

<span data-ttu-id="66ed5-104">**DuplicateBlob** 函式會複製特定的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="66ed5-104">The **DuplicateBlob** function copies a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ed5-105">語法</span><span class="sxs-lookup"><span data-stu-id="66ed5-105">Syntax</span></span>


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="66ed5-106">參數</span><span class="sxs-lookup"><span data-stu-id="66ed5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ed5-107">*hSrcBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66ed5-107">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66ed5-108">複製之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="66ed5-108">Handle to the BLOB that is copied.</span></span>

</dd> <dt>

<span data-ttu-id="66ed5-109">*hBlobThatWillBeCreated* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="66ed5-109">*hBlobThatWillBeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66ed5-110">複製 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="66ed5-110">Handle to the duplicate BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ed5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="66ed5-111">Return value</span></span>

<span data-ttu-id="66ed5-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="66ed5-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="66ed5-113">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="66ed5-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ed5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="66ed5-114">Requirements</span></span>



| <span data-ttu-id="66ed5-115">需求</span><span class="sxs-lookup"><span data-stu-id="66ed5-115">Requirement</span></span> | <span data-ttu-id="66ed5-116">值</span><span class="sxs-lookup"><span data-stu-id="66ed5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66ed5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66ed5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="66ed5-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66ed5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="66ed5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66ed5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="66ed5-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66ed5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66ed5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="66ed5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="66ed5-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="66ed5-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="66ed5-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="66ed5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="66ed5-124"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66ed5-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="66ed5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="66ed5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66ed5-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66ed5-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ed5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66ed5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ed5-128">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="66ed5-128">CreateBlob</span></span>](createblob.md)
</dt> <dt>

[<span data-ttu-id="66ed5-129">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="66ed5-129">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




