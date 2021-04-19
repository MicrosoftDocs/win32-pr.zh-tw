---
description: Register 匯出函式必須在所有剖析器 Dll 中實作為。 註冊的執行會建立並填入通訊協定的屬性資料庫。 網路監視器會使用資料庫來判斷通訊協定支援的屬性。
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: '將剖析器回呼函式註冊 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974624"
---
# <a name="register-parser-callback-function"></a><span data-ttu-id="db7b6-105">註冊剖析器回呼函數</span><span class="sxs-lookup"><span data-stu-id="db7b6-105">Register Parser callback function</span></span>

<span data-ttu-id="db7b6-106">**Register** 匯出函式必須在所有剖析器 dll 中實作為。</span><span class="sxs-lookup"><span data-stu-id="db7b6-106">The **Register** export function must be implemented in all parser DLLs.</span></span> <span data-ttu-id="db7b6-107">**註冊** 的執行會建立並填入通訊協定的 [*屬性資料庫*](p.md)。</span><span class="sxs-lookup"><span data-stu-id="db7b6-107">The implementation of **Register** creates and fills-in a [*property database*](p.md) for a protocol.</span></span> <span data-ttu-id="db7b6-108">網路監視器會使用資料庫來判斷通訊協定支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="db7b6-108">Network Monitor uses the database to determine which properties the protocol supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7b6-109">語法</span><span class="sxs-lookup"><span data-stu-id="db7b6-109">Syntax</span></span>


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="db7b6-110">參數</span><span class="sxs-lookup"><span data-stu-id="db7b6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7b6-111">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db7b6-111">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db7b6-112">呼叫 **Register** 時網路監視器提供的通訊協定控制碼。</span><span class="sxs-lookup"><span data-stu-id="db7b6-112">The handle of the protocol that Network Monitor provides when calling **Register**.</span></span> <span data-ttu-id="db7b6-113">呼叫匯出 helper 函式時，需要 *hProtocol* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="db7b6-113">The *hProtocol* handle is needed when calling export helper functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7b6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="db7b6-114">Return value</span></span>

<span data-ttu-id="db7b6-115">無。</span><span class="sxs-lookup"><span data-stu-id="db7b6-115">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7b6-116">備註</span><span class="sxs-lookup"><span data-stu-id="db7b6-116">Remarks</span></span>

<span data-ttu-id="db7b6-117">一旦載入 capture，網路監視器開始呼叫 **Register** 函數。</span><span class="sxs-lookup"><span data-stu-id="db7b6-117">Network Monitor starts calling the **Register** function as soon as a capture is loaded.</span></span> <span data-ttu-id="db7b6-118">網路監視器會針對它可以識別的每個通訊協定呼叫 **Register** 函數。</span><span class="sxs-lookup"><span data-stu-id="db7b6-118">Network Monitor calls the **Register** function for each protocol it can identify.</span></span> <span data-ttu-id="db7b6-119">[CreateProtocol](createprotocol.md)函式會將指標傳遞至 **Register** 函數。</span><span class="sxs-lookup"><span data-stu-id="db7b6-119">The [CreateProtocol](createprotocol.md) function passes a pointer to the **Register** function.</span></span>

<span data-ttu-id="db7b6-120">**註冊** 的執行包含對下列函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="db7b6-120">The implementation of **Register** includes calls to the following functions.</span></span>

-   <span data-ttu-id="db7b6-121">呼叫 [CreatePropertyDatabase](createpropertydatabase.md) 和 [AddProperty](/previous-versions/bb251873(v=msdn.10)) 函式，以建立該通訊協定支援之所有屬性的資料庫。</span><span class="sxs-lookup"><span data-stu-id="db7b6-121">A call to the [CreatePropertyDatabase](createpropertydatabase.md) and [AddProperty](/previous-versions/bb251873(v=msdn.10)) functions to create a database of all the properties that the protocol supports.</span></span>
-   <span data-ttu-id="db7b6-122">如果通訊協定使用 [*遞交集*](h.md)，則需要呼叫 [CreateHandoffTable](createhandofftable.md)函數。</span><span class="sxs-lookup"><span data-stu-id="db7b6-122">A call to the [CreateHandoffTable](createhandofftable.md) function is required if the protocol uses a [*handoff set*](h.md).</span></span>

<span data-ttu-id="db7b6-123">如果剖析器 DLL 包含多個剖析器，且剖析器可以偵測到一個以上的通訊協定，您必須針對每個通訊協定執行 **Register** 函式。</span><span class="sxs-lookup"><span data-stu-id="db7b6-123">If the parser DLL contains multiple parsers, and the parser can detect more than one protocol, you must implement a **Register** function for each protocol.</span></span>



| <span data-ttu-id="db7b6-124">的相關資訊</span><span class="sxs-lookup"><span data-stu-id="db7b6-124">For Information on</span></span>                                        | <span data-ttu-id="db7b6-125">請參閱</span><span class="sxs-lookup"><span data-stu-id="db7b6-125">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="db7b6-126">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="db7b6-126">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="db7b6-127">解析 器</span><span class="sxs-lookup"><span data-stu-id="db7b6-127">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="db7b6-128">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="db7b6-128">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="db7b6-129">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="db7b6-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="db7b6-130">如何執行 **註冊**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="db7b6-130">How to implement **Register**  includes an example.</span></span>       | [<span data-ttu-id="db7b6-131">執行註冊</span><span class="sxs-lookup"><span data-stu-id="db7b6-131">Implementing Register</span></span>](implementing-register.md)     |



 

## <a name="requirements"></a><span data-ttu-id="db7b6-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="db7b6-132">Requirements</span></span>



| <span data-ttu-id="db7b6-133">需求</span><span class="sxs-lookup"><span data-stu-id="db7b6-133">Requirement</span></span> | <span data-ttu-id="db7b6-134">值</span><span class="sxs-lookup"><span data-stu-id="db7b6-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db7b6-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db7b6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="db7b6-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db7b6-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="db7b6-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db7b6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="db7b6-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db7b6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="db7b6-139">標頭</span><span class="sxs-lookup"><span data-stu-id="db7b6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="db7b6-140"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="db7b6-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db7b6-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db7b6-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="db7b6-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="db7b6-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="db7b6-143">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="db7b6-143">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> <dt>

[<span data-ttu-id="db7b6-144">CreatePropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="db7b6-144">CreatePropertyDatabase</span></span>](createpropertydatabase.md)
</dt> <dt>

[<span data-ttu-id="db7b6-145">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="db7b6-145">CreateProtocol</span></span>](createprotocol.md)
</dt> </dl>

 

