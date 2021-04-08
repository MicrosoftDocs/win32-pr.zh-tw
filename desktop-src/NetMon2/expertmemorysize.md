---
description: ExpertMemorySize 函數會傳回 ExpertAllocMemory 函數所配置的記憶體數量。
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: 'ExpertMemorySize 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847741"
---
# <a name="expertmemorysize-function"></a><span data-ttu-id="e6618-103">ExpertMemorySize 函式</span><span class="sxs-lookup"><span data-stu-id="e6618-103">ExpertMemorySize function</span></span>

<span data-ttu-id="e6618-104">**ExpertMemorySize** 函數會傳回 [ExpertAllocMemory](expertallocmemory.md)函數所配置的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="e6618-104">The **ExpertMemorySize** function returns the amount of memory allocated by the [ExpertAllocMemory](expertallocmemory.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6618-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6618-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a><span data-ttu-id="e6618-106">參數</span><span class="sxs-lookup"><span data-stu-id="e6618-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6618-107">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6618-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6618-108">獨特的專家識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6618-108">Unique expert identifier.</span></span> <span data-ttu-id="e6618-109">網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="e6618-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e6618-110">*pOriginalMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6618-110">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6618-111">[ExpertAllocMemory](expertallocmemory.md)所配置專家的記憶體位址指標。</span><span class="sxs-lookup"><span data-stu-id="e6618-111">Pointer to the memory address of the expert allocated by [ExpertAllocMemory](expertallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6618-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6618-112">Return value</span></span>

<span data-ttu-id="e6618-113">函數會傳回配置的記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e6618-113">The function returns the amount of allocated memory   in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6618-114">備註</span><span class="sxs-lookup"><span data-stu-id="e6618-114">Remarks</span></span>

<span data-ttu-id="e6618-115">如需 **ExpertMemorySize** 所傳回之 **大小 \_ T** 資料類型的相關資訊，請參閱資料類型。</span><span class="sxs-lookup"><span data-stu-id="e6618-115">For information on the **SIZE\_T** data type that **ExpertMemorySize** returns, see Data Types.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6618-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6618-116">Requirements</span></span>



| <span data-ttu-id="e6618-117">需求</span><span class="sxs-lookup"><span data-stu-id="e6618-117">Requirement</span></span> | <span data-ttu-id="e6618-118">值</span><span class="sxs-lookup"><span data-stu-id="e6618-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6618-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6618-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6618-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6618-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e6618-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6618-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6618-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6618-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e6618-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e6618-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6618-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e6618-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e6618-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6618-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6618-126"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6618-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6618-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e6618-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6618-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6618-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




