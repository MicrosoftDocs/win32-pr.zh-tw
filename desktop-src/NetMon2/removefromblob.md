---
description: RemoveFromBlob 函式會刪除任何層級的 BLOB 專案 (擁有者、類別或標記) 。
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: 'RemoveFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972839"
---
# <a name="removefromblob-function"></a><span data-ttu-id="1f69d-103">RemoveFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="1f69d-103">RemoveFromBlob function</span></span>

<span data-ttu-id="1f69d-104">**RemoveFromBlob** 函式會刪除任何層級的 BLOB 專案 (**擁有** 者、**類別** 或 **標記**) 。</span><span class="sxs-lookup"><span data-stu-id="1f69d-104">The **RemoveFromBlob** function deletes any level of BLOB entry (**Owner**, **Category**, or **Tag**).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f69d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f69d-105">Syntax</span></span>


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a><span data-ttu-id="1f69d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f69d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f69d-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-108">要從中刪除專案之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f69d-108">Handle to the BLOB from which an entry is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-110">**擁有** 者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1f69d-110">Pointer to the **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-112">**類別目錄** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1f69d-112">Pointer to the **Category** name.</span></span> <span data-ttu-id="1f69d-113">**Null** 參數值表示呼叫端正在嘗試刪除指定的 **擁有** 者資訊及其所有子專案。</span><span class="sxs-lookup"><span data-stu-id="1f69d-113">A **NULL** parameter value indicates the caller is attempting to delete the given **Owner** information and all of its child entries.</span></span> <span data-ttu-id="1f69d-114">請注意，如果 *pCategoryName* 參數值為 **null**， *PTagName* 參數也必須是 **null**。</span><span class="sxs-lookup"><span data-stu-id="1f69d-114">Note that if the *pCategoryName* parameter value is **NULL**, the *pTagName* parameter must also be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-115">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-115">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-116">**標記** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1f69d-116">Pointer to the **Tag** name.</span></span> <span data-ttu-id="1f69d-117">**Null**_pTagName_ 值表示呼叫端正在嘗試刪除指定的 **類別** 及其所有子專案。</span><span class="sxs-lookup"><span data-stu-id="1f69d-117">A **NULL**_pTagName_ value indicates the caller is attempting to delete the given **Category** and all of its child entries.</span></span> <span data-ttu-id="1f69d-118">如果參數值不是 **Null**，則呼叫端會要求只刪除指定的 **標記** 專案。</span><span class="sxs-lookup"><span data-stu-id="1f69d-118">If the parameter value is not **NULL**, the caller is asking that only that the specified **Tag** entries be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f69d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f69d-119">Return value</span></span>

<span data-ttu-id="1f69d-120">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="1f69d-120">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1f69d-121">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="1f69d-121">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f69d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f69d-122">Requirements</span></span>



| <span data-ttu-id="1f69d-123">需求</span><span class="sxs-lookup"><span data-stu-id="1f69d-123">Requirement</span></span> | <span data-ttu-id="1f69d-124">值</span><span class="sxs-lookup"><span data-stu-id="1f69d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f69d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f69d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1f69d-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1f69d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f69d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1f69d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f69d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1f69d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f69d-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1f69d-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1f69d-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f69d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f69d-132"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f69d-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f69d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1f69d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f69d-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f69d-134"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




