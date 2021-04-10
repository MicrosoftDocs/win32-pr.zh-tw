---
description: 傳回應用程式協定資料單位的 Le 欄位， (APDU) 。
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'ISCardCmd：： get_LeField 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695383"
---
# <a name="iscardcmdget_lefield-method"></a><span data-ttu-id="d018e-103">ISCardCmd：： get \_ LeField 方法</span><span class="sxs-lookup"><span data-stu-id="d018e-103">ISCardCmd::get\_LeField method</span></span>

<span data-ttu-id="d018e-104">\[**Get \_ LeField** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d018e-104">\[The **get\_LeField** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d018e-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d018e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d018e-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d018e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d018e-107">**Get \_ LeField** 方法會傳回 [*應用程式協定資料單位*](../secgloss/a-gly.md)的 Le 欄位， (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="d018e-107">The **get\_LeField** method returns the Le field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="d018e-108">語法</span><span class="sxs-lookup"><span data-stu-id="d018e-108">Syntax</span></span>


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="d018e-109">參數</span><span class="sxs-lookup"><span data-stu-id="d018e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d018e-110">*plSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d018e-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d018e-111">傳回時的 Le 域值指標。</span><span class="sxs-lookup"><span data-stu-id="d018e-111">Pointer to the Le field value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d018e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d018e-112">Return value</span></span>

<span data-ttu-id="d018e-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="d018e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d018e-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d018e-114">Return code</span></span>                                                                                  | <span data-ttu-id="d018e-115">Description</span><span class="sxs-lookup"><span data-stu-id="d018e-115">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d018e-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d018e-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d018e-117">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="d018e-117">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d018e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d018e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d018e-119">*PlSize* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="d018e-119">The *plSize* parameter is not valid.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="d018e-120">範例</span><span class="sxs-lookup"><span data-stu-id="d018e-120">Examples</span></span>

<span data-ttu-id="d018e-121">下列範例示範如何從 [*應用程式協定資料單位*](../secgloss/a-gly.md) 中取出 Le 域值 (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="d018e-121">The following example shows how to retrieve the Le field value from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="d018e-122">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="d018e-122">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a><span data-ttu-id="d018e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d018e-123">Requirements</span></span>



| <span data-ttu-id="d018e-124">需求</span><span class="sxs-lookup"><span data-stu-id="d018e-124">Requirement</span></span> | <span data-ttu-id="d018e-125">值</span><span class="sxs-lookup"><span data-stu-id="d018e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d018e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d018e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d018e-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d018e-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d018e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d018e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d018e-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d018e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d018e-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d018e-130">End of client support</span></span><br/>    | <span data-ttu-id="d018e-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d018e-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d018e-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d018e-132">End of server support</span></span><br/>    | <span data-ttu-id="d018e-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d018e-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d018e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d018e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d018e-135"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="d018e-135"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d018e-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d018e-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="d018e-137"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d018e-137"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d018e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d018e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d018e-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d018e-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d018e-140">IID</span><span class="sxs-lookup"><span data-stu-id="d018e-140">IID</span></span><br/>                      | <span data-ttu-id="d018e-141">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d018e-141">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d018e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d018e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d018e-143">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="d018e-143">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
