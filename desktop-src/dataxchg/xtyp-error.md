---
title: 'XTYP_ERROR 交易 (Ddeml .h) '
description: 當發生重大錯誤時，動態資料交換 (DDE) 回呼函式 DdeCallback 會接收 XTYP \_ 錯誤交易。
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967733"
---
# <a name="xtyp_error-transaction"></a><span data-ttu-id="253e6-104">XTYP \_ 錯誤交易</span><span class="sxs-lookup"><span data-stu-id="253e6-104">XTYP\_ERROR transaction</span></span>

<span data-ttu-id="253e6-105">當發生重大錯誤時，動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 **XTYP \_ 錯誤** 交易。</span><span class="sxs-lookup"><span data-stu-id="253e6-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_ERROR** transaction when a critical error occurs.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="253e6-106">參數</span><span class="sxs-lookup"><span data-stu-id="253e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="253e6-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="253e6-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-108">交易類型。</span><span class="sxs-lookup"><span data-stu-id="253e6-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="253e6-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="253e6-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="253e6-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="253e6-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="253e6-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-112">與錯誤相關聯之交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="253e6-112">A handle to the conversation associated with the error.</span></span> <span data-ttu-id="253e6-113">如果錯誤未與交談相關聯，此參數為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="253e6-113">This parameter is **NULL** if the error is not associated with a conversation.</span></span>

</dd> <dt>

<span data-ttu-id="253e6-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="253e6-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="253e6-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="253e6-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="253e6-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="253e6-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="253e6-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="253e6-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-119">未使用。</span><span class="sxs-lookup"><span data-stu-id="253e6-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="253e6-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="253e6-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-121">低序位單字的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="253e6-121">The error code in the low-order word.</span></span> <span data-ttu-id="253e6-122">目前僅支援下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="253e6-122">Currently, only the following error code is supported.</span></span>



| <span data-ttu-id="253e6-123">值</span><span class="sxs-lookup"><span data-stu-id="253e6-123">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="253e6-124">意義</span><span class="sxs-lookup"><span data-stu-id="253e6-124">Meaning</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <span data-ttu-id="253e6-125"><dt>**DMLERR \_ \_ 記憶體不足**</dt></span><span class="sxs-lookup"><span data-stu-id="253e6-125"><dt>**DMLERR\_LOW\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="253e6-126">記憶體偏低;建議、執行資料可能會遺失，或者系統可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="253e6-126">Memory is low; advise, poke, or execute data may be lost, or the system may fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="253e6-127">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="253e6-127">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="253e6-128">未使用。</span><span class="sxs-lookup"><span data-stu-id="253e6-128">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="253e6-129">備註</span><span class="sxs-lookup"><span data-stu-id="253e6-129">Remarks</span></span>

<span data-ttu-id="253e6-130">應用程式無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="253e6-130">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span> <span data-ttu-id="253e6-131">動態資料交換管理程式庫 (DDEML) 藉由移除非關鍵的資源來嘗試釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="253e6-131">The Dynamic Data Exchange Management Library (DDEML) attempts to free memory by removing noncritical resources.</span></span> <span data-ttu-id="253e6-132">已封鎖交談的應用程式應該將其解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="253e6-132">An application that has blocked conversations should unblock them.</span></span>

## <a name="requirements"></a><span data-ttu-id="253e6-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="253e6-133">Requirements</span></span>



| <span data-ttu-id="253e6-134">需求</span><span class="sxs-lookup"><span data-stu-id="253e6-134">Requirement</span></span> | <span data-ttu-id="253e6-135">值</span><span class="sxs-lookup"><span data-stu-id="253e6-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="253e6-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="253e6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="253e6-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="253e6-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="253e6-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="253e6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="253e6-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="253e6-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="253e6-140">標頭</span><span class="sxs-lookup"><span data-stu-id="253e6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="253e6-141"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="253e6-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="253e6-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="253e6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253e6-143">動態資料交換管理程式庫總覽</span><span class="sxs-lookup"><span data-stu-id="253e6-143">Dynamic Data Exchange Management Library Overview</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

