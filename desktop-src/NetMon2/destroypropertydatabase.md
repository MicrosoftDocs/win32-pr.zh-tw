---
description: DestroyPropertyDatabase 函式會釋放用來建立通訊協定屬性資料庫的資源。
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: 'DestroyPropertyDatabase 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945135"
---
# <a name="destroypropertydatabase-function"></a><span data-ttu-id="d49c2-103">DestroyPropertyDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="d49c2-103">DestroyPropertyDatabase function</span></span>

<span data-ttu-id="d49c2-104">**DestroyPropertyDatabase** 函式會釋放用來建立通訊協定 [*屬性資料庫*](p.md)的資源。</span><span class="sxs-lookup"><span data-stu-id="d49c2-104">The **DestroyPropertyDatabase** function releases the resources used to create the protocol [*property database*](p.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d49c2-105">語法</span><span class="sxs-lookup"><span data-stu-id="d49c2-105">Syntax</span></span>


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d49c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="d49c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d49c2-107">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d49c2-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d49c2-108">要終結之屬性資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d49c2-108">Handle to the property database to be destroyed.</span></span> <span data-ttu-id="d49c2-109">當網路監視器呼叫取消 [註冊](deregister.md) 函式時，會將控制碼傳遞給剖析器 DLL。</span><span class="sxs-lookup"><span data-stu-id="d49c2-109">The handle is passed to the parser DLL when Network Monitor calls the [Deregister](deregister.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d49c2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d49c2-110">Return value</span></span>

<span data-ttu-id="d49c2-111">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="d49c2-111">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d49c2-112">如果函式不成功，則傳回值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d49c2-112">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="d49c2-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d49c2-113">Return code</span></span>                                                                                              | <span data-ttu-id="d49c2-114">Description</span><span class="sxs-lookup"><span data-stu-id="d49c2-114">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="d49c2-115"><dt>**NMERR \_ 內部 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="d49c2-115"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="d49c2-116">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="d49c2-116">An internal error occurred.</span></span> <br/>    |
| <dl> <span data-ttu-id="d49c2-117"><dt>**NMERR \_ 不正確 \_ HPROTOCOL**</dt></span><span class="sxs-lookup"><span data-stu-id="d49c2-117"><dt>**NMERR\_INVALID\_HPROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="d49c2-118">*HProtocol* 中的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="d49c2-118">Invalid handle in *hProtocol*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="d49c2-119">備註</span><span class="sxs-lookup"><span data-stu-id="d49c2-119">Remarks</span></span>

<span data-ttu-id="d49c2-120">只有在為通訊協定執行取消 [註冊](deregister.md)匯出函數時，才應該呼叫 **DestroyPropertyDatabase** 函式。</span><span class="sxs-lookup"><span data-stu-id="d49c2-120">The **DestroyPropertyDatabase** function should be called only when implementing the [Deregister](deregister.md) export function for the protocol.</span></span> <span data-ttu-id="d49c2-121">針對支援多個通訊協定的剖析器 Dll，會針對每個取消 **註冊** 的執行呼叫 **DestroyPropertyDatabase** 函數。</span><span class="sxs-lookup"><span data-stu-id="d49c2-121">For parser DLLs that support multiple protocols, the **DestroyPropertyDatabase** function is called for each implementation of **Deregister**.</span></span>



| <span data-ttu-id="d49c2-122">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="d49c2-122">For information on</span></span>                                        | <span data-ttu-id="d49c2-123">請參閱</span><span class="sxs-lookup"><span data-stu-id="d49c2-123">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="d49c2-124">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="d49c2-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="d49c2-125">解析 器</span><span class="sxs-lookup"><span data-stu-id="d49c2-125">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="d49c2-126">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="d49c2-126">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="d49c2-127">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="d49c2-127">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="d49c2-128">如何執行取消 **註冊**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="d49c2-128">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="d49c2-129">執行取消註冊</span><span class="sxs-lookup"><span data-stu-id="d49c2-129">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="d49c2-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d49c2-130">Requirements</span></span>



| <span data-ttu-id="d49c2-131">需求</span><span class="sxs-lookup"><span data-stu-id="d49c2-131">Requirement</span></span> | <span data-ttu-id="d49c2-132">值</span><span class="sxs-lookup"><span data-stu-id="d49c2-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d49c2-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d49c2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d49c2-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d49c2-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d49c2-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d49c2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d49c2-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d49c2-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d49c2-137">標頭</span><span class="sxs-lookup"><span data-stu-id="d49c2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d49c2-138"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="d49c2-138"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d49c2-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="d49c2-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="d49c2-140"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d49c2-140"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d49c2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d49c2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d49c2-142"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d49c2-142"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d49c2-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d49c2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49c2-144">取消註冊</span><span class="sxs-lookup"><span data-stu-id="d49c2-144">Deregister</span></span>](deregister.md)
</dt> </dl>

 

 




