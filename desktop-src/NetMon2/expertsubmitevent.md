---
description: ExpertSubmitEvent 函式會指出事件條件存在，並提供描述條件的資料結構。
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: 'ExpertSubmitEvent 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318080"
---
# <a name="expertsubmitevent-function"></a><span data-ttu-id="98de9-103">ExpertSubmitEvent 函式</span><span class="sxs-lookup"><span data-stu-id="98de9-103">ExpertSubmitEvent function</span></span>

<span data-ttu-id="98de9-104">**ExpertSubmitEvent** 函式會指出事件條件存在，並提供描述條件的資料結構。</span><span class="sxs-lookup"><span data-stu-id="98de9-104">The **ExpertSubmitEvent** function indicates that an event condition exists and provides a data structure that describes the condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="98de9-105">語法</span><span class="sxs-lookup"><span data-stu-id="98de9-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a><span data-ttu-id="98de9-106">參數</span><span class="sxs-lookup"><span data-stu-id="98de9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98de9-107">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98de9-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98de9-108">專家的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="98de9-108">Unique identifier of the expert.</span></span> <span data-ttu-id="98de9-109">網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="98de9-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="98de9-110">*pExpertEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98de9-110">*pExpertEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98de9-111">描述事件條件之 **NMEVENTDATA** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="98de9-111">A pointer to an **NMEVENTDATA** structure that describes the event condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98de9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="98de9-112">Return value</span></span>

<span data-ttu-id="98de9-113">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="98de9-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="98de9-114">如果函式不成功，則傳回值會指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="98de9-114">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="98de9-115">如果傳回值是 NMERR \_ 專家 \_ 終止，則專家會立即清除並返回。</span><span class="sxs-lookup"><span data-stu-id="98de9-115">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="98de9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="98de9-116">Requirements</span></span>



| <span data-ttu-id="98de9-117">需求</span><span class="sxs-lookup"><span data-stu-id="98de9-117">Requirement</span></span> | <span data-ttu-id="98de9-118">值</span><span class="sxs-lookup"><span data-stu-id="98de9-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98de9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98de9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98de9-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98de9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="98de9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98de9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98de9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98de9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="98de9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="98de9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98de9-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="98de9-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="98de9-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="98de9-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="98de9-126"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="98de9-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="98de9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="98de9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98de9-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98de9-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




