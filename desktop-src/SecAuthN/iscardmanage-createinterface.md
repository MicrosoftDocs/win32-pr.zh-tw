---
description: 建立指定的介面。
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: ISCardManage：： CreateInterface 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194074"
---
# <a name="iscardmanagecreateinterface-method"></a><span data-ttu-id="00b2e-103">ISCardManage：： CreateInterface 方法</span><span class="sxs-lookup"><span data-stu-id="00b2e-103">ISCardManage::CreateInterface method</span></span>

<span data-ttu-id="00b2e-104">\[**CreateInterface** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="00b2e-104">\[The **CreateInterface** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00b2e-105">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="00b2e-106">**CreateInterface** 方法會建立指定的介面。</span><span class="sxs-lookup"><span data-stu-id="00b2e-106">The **CreateInterface** method creates the specified interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b2e-107">語法</span><span class="sxs-lookup"><span data-stu-id="00b2e-107">Syntax</span></span>


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a><span data-ttu-id="00b2e-108">參數</span><span class="sxs-lookup"><span data-stu-id="00b2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00b2e-109">*pguidInterface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-109">*pguidInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00b2e-110">要建立之介面的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="00b2e-110">The GUID value of the interface to create.</span></span>

</dd> <dt>

<span data-ttu-id="00b2e-111">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00b2e-112">GUID 無法使用時所要建立的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="00b2e-112">The name of the interface to create if the GUID is unavailable.</span></span> <span data-ttu-id="00b2e-113">標準值為 "CryptoProvider"。</span><span class="sxs-lookup"><span data-stu-id="00b2e-113">Standard values are "CryptoProvider".</span></span>

</dd> <dt>

<span data-ttu-id="00b2e-114">*pUserData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-114">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00b2e-115">要在建立介面時使用之使用者特定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="00b2e-115">Pointer to user-specific data to use in the creation of an interface.</span></span>

</dd> <dt>

<span data-ttu-id="00b2e-116">*ppInterface* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-116">*ppInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00b2e-117">傳回之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="00b2e-117">Pointer to the returned interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00b2e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="00b2e-118">Return value</span></span>

<span data-ttu-id="00b2e-119">可能的傳回值如下：</span><span class="sxs-lookup"><span data-stu-id="00b2e-119">The possible return values are the following:</span></span>



| <span data-ttu-id="00b2e-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="00b2e-120">Return code</span></span>                                                                                   | <span data-ttu-id="00b2e-121">Description</span><span class="sxs-lookup"><span data-stu-id="00b2e-121">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00b2e-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="00b2e-123">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="00b2e-123">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="00b2e-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="00b2e-125">其中一個提供的參數無效。</span><span class="sxs-lookup"><span data-stu-id="00b2e-125">One of the supplied parameters are not valid.</span></span><br/>                                         |
| <dl> <span data-ttu-id="00b2e-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="00b2e-127">在 *pguidInterface* 或 *pUserData* 參數中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="00b2e-127">A bad pointer was passed in either the *pguidInterface* or the *pUserData* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="00b2e-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="00b2e-129">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="00b2e-129">Out of memory.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="00b2e-130">備註</span><span class="sxs-lookup"><span data-stu-id="00b2e-130">Remarks</span></span>

<span data-ttu-id="00b2e-131">如需 [**ISCardManage**](iscardmanage.md) 介面所定義之所有方法的清單，請參閱 **ISCardManage**。</span><span class="sxs-lookup"><span data-stu-id="00b2e-131">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see **ISCardManage**.</span></span>

<span data-ttu-id="00b2e-132">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00b2e-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="00b2e-133">如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="00b2e-133">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00b2e-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="00b2e-134">Requirements</span></span>



| <span data-ttu-id="00b2e-135">需求</span><span class="sxs-lookup"><span data-stu-id="00b2e-135">Requirement</span></span> | <span data-ttu-id="00b2e-136">值</span><span class="sxs-lookup"><span data-stu-id="00b2e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="00b2e-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00b2e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="00b2e-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="00b2e-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00b2e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="00b2e-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="00b2e-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="00b2e-141">End of client support</span></span><br/>    | <span data-ttu-id="00b2e-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00b2e-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="00b2e-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="00b2e-143">End of server support</span></span><br/>    | <span data-ttu-id="00b2e-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00b2e-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="00b2e-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00b2e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b2e-146">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="00b2e-146">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
