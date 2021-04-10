---
description: DestroyHandoffTable 函式會終結以 CreateHandoffTable 建立的遞交資料表。
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: 'DestroyHandoffTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944144"
---
# <a name="destroyhandofftable-function"></a><span data-ttu-id="1cab2-103">DestroyHandoffTable 函式</span><span class="sxs-lookup"><span data-stu-id="1cab2-103">DestroyHandoffTable function</span></span>

<span data-ttu-id="1cab2-104">**DestroyHandoffTable** 函式會終結以 **CreateHandoffTable** 建立的遞交資料表。</span><span class="sxs-lookup"><span data-stu-id="1cab2-104">The **DestroyHandoffTable** function destroys a handoff table created with **CreateHandoffTable**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cab2-105">語法</span><span class="sxs-lookup"><span data-stu-id="1cab2-105">Syntax</span></span>


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a><span data-ttu-id="1cab2-106">參數</span><span class="sxs-lookup"><span data-stu-id="1cab2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cab2-107">*hTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cab2-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cab2-108">損毀的交付資料表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cab2-108">Handle to the destroyed handoff table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cab2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cab2-109">Return value</span></span>

<span data-ttu-id="1cab2-110">無。</span><span class="sxs-lookup"><span data-stu-id="1cab2-110">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cab2-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cab2-111">Requirements</span></span>



| <span data-ttu-id="1cab2-112">需求</span><span class="sxs-lookup"><span data-stu-id="1cab2-112">Requirement</span></span> | <span data-ttu-id="1cab2-113">值</span><span class="sxs-lookup"><span data-stu-id="1cab2-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1cab2-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cab2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1cab2-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cab2-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1cab2-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cab2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1cab2-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cab2-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1cab2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1cab2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cab2-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1cab2-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1cab2-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="1cab2-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cab2-121"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cab2-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1cab2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1cab2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cab2-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cab2-123"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




