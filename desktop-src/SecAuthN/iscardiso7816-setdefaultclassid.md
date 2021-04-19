---
description: SetDefaultClassId 方法會指派標準類別識別碼位元組，以在建立 ISO 7816-4 命令應用程式協定資料單位 (APDU) 時用於所有作業。 標準類別識別碼的位元組預設為0x00。
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'ISCardISO7816：： SetDefaultClassId 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997541"
---
# <a name="iscardiso7816setdefaultclassid-method"></a><span data-ttu-id="c44e6-104">ISCardISO7816：： SetDefaultClassId 方法</span><span class="sxs-lookup"><span data-stu-id="c44e6-104">ISCardISO7816::SetDefaultClassId method</span></span>

<span data-ttu-id="c44e6-105">\[**SetDefaultClassId** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c44e6-105">\[The **SetDefaultClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c44e6-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="c44e6-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c44e6-107">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c44e6-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c44e6-108">**SetDefaultClassId** 方法會指派標準類別識別碼位元組，以在建立 ISO 7816-4 命令 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 時用於所有作業。</span><span class="sxs-lookup"><span data-stu-id="c44e6-108">The **SetDefaultClassId** method assigns a standard class identifier byte that will be used in all operations when constructing an ISO 7816-4 command [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="c44e6-109">標準類別識別碼的位元組預設為0x00。</span><span class="sxs-lookup"><span data-stu-id="c44e6-109">By default, the standard class identifier byte is 0x00.</span></span>

## <a name="syntax"></a><span data-ttu-id="c44e6-110">語法</span><span class="sxs-lookup"><span data-stu-id="c44e6-110">Syntax</span></span>


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="c44e6-111">參數</span><span class="sxs-lookup"><span data-stu-id="c44e6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c44e6-112">*byClass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c44e6-112">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c44e6-113">類別識別碼位元組。</span><span class="sxs-lookup"><span data-stu-id="c44e6-113">Class ID byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c44e6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c44e6-114">Return value</span></span>

<span data-ttu-id="c44e6-115">可能的傳回值如下：</span><span class="sxs-lookup"><span data-stu-id="c44e6-115">The possible return values are the following:</span></span>



| <span data-ttu-id="c44e6-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c44e6-116">Return code</span></span>                                                                          | <span data-ttu-id="c44e6-117">Description</span><span class="sxs-lookup"><span data-stu-id="c44e6-117">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c44e6-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c44e6-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c44e6-119">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="c44e6-119">Operation completed successfully.</span></span><br/> |



 

<span data-ttu-id="c44e6-120">如需 [**ISCardISO7816**](iscardiso7816.md) 介面所提供的所有方法清單，請參閱 **ISCardISO7816**。</span><span class="sxs-lookup"><span data-stu-id="c44e6-120">For a list of all the methods provided by the [**ISCardISO7816**](iscardiso7816.md) interface, see **ISCardISO7816**.</span></span>

<span data-ttu-id="c44e6-121">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c44e6-121">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c44e6-122">如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="c44e6-122">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c44e6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c44e6-123">Requirements</span></span>



| <span data-ttu-id="c44e6-124">需求</span><span class="sxs-lookup"><span data-stu-id="c44e6-124">Requirement</span></span> | <span data-ttu-id="c44e6-125">值</span><span class="sxs-lookup"><span data-stu-id="c44e6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c44e6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c44e6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c44e6-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c44e6-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c44e6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c44e6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c44e6-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c44e6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c44e6-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c44e6-130">End of client support</span></span><br/>    | <span data-ttu-id="c44e6-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c44e6-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c44e6-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c44e6-132">End of server support</span></span><br/>    | <span data-ttu-id="c44e6-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c44e6-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c44e6-134">標頭</span><span class="sxs-lookup"><span data-stu-id="c44e6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c44e6-135"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c44e6-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c44e6-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c44e6-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="c44e6-137"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c44e6-137"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c44e6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c44e6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c44e6-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c44e6-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c44e6-140">IID</span><span class="sxs-lookup"><span data-stu-id="c44e6-140">IID</span></span><br/>                      | <span data-ttu-id="c44e6-141">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c44e6-141">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c44e6-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c44e6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c44e6-143">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="c44e6-143">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
