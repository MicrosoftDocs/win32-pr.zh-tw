---
description: 指定要搭配 ISCardCmd 介面使用 (Nad) 的節點位址。
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd：:p ut_Nad 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848364"
---
# <a name="iscardcmdput_nad-method"></a><span data-ttu-id="af48c-103">ISCardCmd：:p 的 \_ Nad Nad 方法</span><span class="sxs-lookup"><span data-stu-id="af48c-103">ISCardCmd::put\_Nad method</span></span>

<span data-ttu-id="af48c-104">\[**Put \_ Nad** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="af48c-104">\[The **put\_Nad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af48c-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="af48c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af48c-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="af48c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="af48c-107">**Put \_ Nad** 方法會指定要搭配 [**ISCardCmd**](iscardcmd.md)介面使用 (Nad) 的節點位址。</span><span class="sxs-lookup"><span data-stu-id="af48c-107">The **put\_Nad** method specifies the node address (Nad) to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="af48c-108">這僅適用于使用 [*T = 1 通訊協定*](../secgloss/t-gly.md) 通訊的通訊。</span><span class="sxs-lookup"><span data-stu-id="af48c-108">This applies to communications using the [*T=1 protocol*](../secgloss/t-gly.md) communications only.</span></span> <span data-ttu-id="af48c-109">根據預設， [**ISCardCmd**](iscardcmd.md) 物件會使用零的 Nad。</span><span class="sxs-lookup"><span data-stu-id="af48c-109">By default, the [**ISCardCmd**](iscardcmd.md) object uses a Nad of zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="af48c-110">語法</span><span class="sxs-lookup"><span data-stu-id="af48c-110">Syntax</span></span>


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a><span data-ttu-id="af48c-111">參數</span><span class="sxs-lookup"><span data-stu-id="af48c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af48c-112">*bNad* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af48c-112">*bNad* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af48c-113">代表要使用之 Nad 的位元組。</span><span class="sxs-lookup"><span data-stu-id="af48c-113">Byte representing the Nad to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af48c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="af48c-114">Return value</span></span>

<span data-ttu-id="af48c-115">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="af48c-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="af48c-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="af48c-116">Return code</span></span>                                                                                  | <span data-ttu-id="af48c-117">Description</span><span class="sxs-lookup"><span data-stu-id="af48c-117">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="af48c-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="af48c-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="af48c-119">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="af48c-119">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="af48c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af48c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="af48c-121">*BNad* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="af48c-121">The *bNad* parameter is not valid.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="af48c-122">備註</span><span class="sxs-lookup"><span data-stu-id="af48c-122">Remarks</span></span>

<span data-ttu-id="af48c-123">只有在需要針對 Nad 使用零以外的值時，才應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="af48c-123">This method should be called only when it is necessary to use a value other than zero for the Nad.</span></span>

## <a name="examples"></a><span data-ttu-id="af48c-124">範例</span><span class="sxs-lookup"><span data-stu-id="af48c-124">Examples</span></span>

<span data-ttu-id="af48c-125">下列範例顯示如何指定要搭配 [**ISCardCmd**](iscardcmd.md) 介面使用的節點位址。</span><span class="sxs-lookup"><span data-stu-id="af48c-125">The following example shows how to specify a node address to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="af48c-126">此範例假設 byNadValue 是先前已指派值的 **BYTE** 類型變數，而該 PISCardCmd 是 **ISCardCmd** 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="af48c-126">The example assumes that byNadValue is a variable of type **BYTE** that was previously assigned a value, and that pISCardCmd is a valid pointer to an instance of the **ISCardCmd** interface.</span></span>


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="af48c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="af48c-127">Requirements</span></span>



| <span data-ttu-id="af48c-128">需求</span><span class="sxs-lookup"><span data-stu-id="af48c-128">Requirement</span></span> | <span data-ttu-id="af48c-129">值</span><span class="sxs-lookup"><span data-stu-id="af48c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af48c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af48c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="af48c-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af48c-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af48c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af48c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="af48c-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af48c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af48c-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="af48c-134">End of client support</span></span><br/>    | <span data-ttu-id="af48c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af48c-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af48c-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="af48c-136">End of server support</span></span><br/>    | <span data-ttu-id="af48c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af48c-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af48c-138">標頭</span><span class="sxs-lookup"><span data-stu-id="af48c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="af48c-139"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="af48c-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="af48c-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="af48c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="af48c-141"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af48c-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af48c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="af48c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af48c-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af48c-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="af48c-144">IID</span><span class="sxs-lookup"><span data-stu-id="af48c-144">IID</span></span><br/>                      | <span data-ttu-id="af48c-145">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="af48c-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="af48c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af48c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af48c-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="af48c-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
