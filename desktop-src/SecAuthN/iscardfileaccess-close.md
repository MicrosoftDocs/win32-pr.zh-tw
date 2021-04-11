---
description: Close 方法會關閉指定的檔案。 不允許進一步存取檔案。
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: ISCardFileAccess：： Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: ac08d62e71045df49503eb4c05fcb5ea273b4cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113205"
---
# <a name="iscardfileaccessclose-method"></a><span data-ttu-id="eeb8a-104">ISCardFileAccess：： Close 方法</span><span class="sxs-lookup"><span data-stu-id="eeb8a-104">ISCardFileAccess::Close method</span></span>

<span data-ttu-id="eeb8a-105">\[**Close** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-105">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eeb8a-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eeb8a-107">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="eeb8a-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="eeb8a-108">**Close** 方法會關閉指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-108">The **Close** method closes the specified file.</span></span> <span data-ttu-id="eeb8a-109">不允許進一步存取檔案。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-109">No further access to file is allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb8a-110">語法</span><span class="sxs-lookup"><span data-stu-id="eeb8a-110">Syntax</span></span>


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="eeb8a-111">參數</span><span class="sxs-lookup"><span data-stu-id="eeb8a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb8a-112">*hFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eeb8a-112">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb8a-113">要關閉之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-113">A handle to the file to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb8a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eeb8a-114">Return value</span></span>

<span data-ttu-id="eeb8a-115">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="eeb8a-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eeb8a-116">Return code</span></span>                                                                                   | <span data-ttu-id="eeb8a-117">Description</span><span class="sxs-lookup"><span data-stu-id="eeb8a-117">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="eeb8a-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eeb8a-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="eeb8a-119">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-119">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="eeb8a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eeb8a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="eeb8a-121">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-121">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="eeb8a-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="eeb8a-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="eeb8a-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="eeb8a-124">備註</span><span class="sxs-lookup"><span data-stu-id="eeb8a-124">Remarks</span></span>

<span data-ttu-id="eeb8a-125">若要開啟檔案，請呼叫 [**open**](iscardfileaccess-open.md)。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-125">To open a file, call [**Open**](iscardfileaccess-open.md).</span></span>

<span data-ttu-id="eeb8a-126">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="eeb8a-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="eeb8a-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="eeb8a-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb8a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeb8a-129">Requirements</span></span>



| <span data-ttu-id="eeb8a-130">需求</span><span class="sxs-lookup"><span data-stu-id="eeb8a-130">Requirement</span></span> | <span data-ttu-id="eeb8a-131">值</span><span class="sxs-lookup"><span data-stu-id="eeb8a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eeb8a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeb8a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb8a-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeb8a-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="eeb8a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeb8a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb8a-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeb8a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="eeb8a-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="eeb8a-136">End of client support</span></span><br/>    | <span data-ttu-id="eeb8a-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eeb8a-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="eeb8a-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="eeb8a-138">End of server support</span></span><br/>    | <span data-ttu-id="eeb8a-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eeb8a-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="eeb8a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeb8a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb8a-141">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-141">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="eeb8a-142">**打開**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-142">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
