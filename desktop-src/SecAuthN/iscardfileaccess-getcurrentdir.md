---
description: GetCurrentDir 方法會傳回目前所選目錄的絕對路徑。
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: ISCardFileAccess：： GetCurrentDir 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: a779dca10a94250bf4b500585b8b50238b0267dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195251"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a><span data-ttu-id="df8d9-103">ISCardFileAccess：： GetCurrentDir 方法</span><span class="sxs-lookup"><span data-stu-id="df8d9-103">ISCardFileAccess::GetCurrentDir method</span></span>

<span data-ttu-id="df8d9-104">\[**GetCurrentDir** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="df8d9-104">\[The **GetCurrentDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="df8d9-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="df8d9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df8d9-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="df8d9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="df8d9-107">**GetCurrentDir** 方法會傳回目前所選目錄的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="df8d9-107">The **GetCurrentDir** method returns an absolute path to the currently selected directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8d9-108">語法</span><span class="sxs-lookup"><span data-stu-id="df8d9-108">Syntax</span></span>


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a><span data-ttu-id="df8d9-109">參數</span><span class="sxs-lookup"><span data-stu-id="df8d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8d9-110">*pbstrPathSpec* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df8d9-110">*pbstrPathSpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df8d9-111">將包含路徑之 BSTR 的指標。</span><span class="sxs-lookup"><span data-stu-id="df8d9-111">Pointer to a BSTR that will contain the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8d9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="df8d9-112">Return value</span></span>

<span data-ttu-id="df8d9-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="df8d9-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="df8d9-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="df8d9-114">Return code</span></span>                                                                                   | <span data-ttu-id="df8d9-115">Description</span><span class="sxs-lookup"><span data-stu-id="df8d9-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="df8d9-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="df8d9-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df8d9-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="df8d9-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="df8d9-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df8d9-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="df8d9-119">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="df8d9-119">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="df8d9-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="df8d9-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="df8d9-121">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="df8d9-121">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="df8d9-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="df8d9-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df8d9-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="df8d9-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="df8d9-124">備註</span><span class="sxs-lookup"><span data-stu-id="df8d9-124">Remarks</span></span>

<span data-ttu-id="df8d9-125">若要變更目前的目錄，請呼叫 [**ChangeDir**](iscardfileaccess-changedir.md)。</span><span class="sxs-lookup"><span data-stu-id="df8d9-125">To change the current directory, call [**ChangeDir**](iscardfileaccess-changedir.md).</span></span>

<span data-ttu-id="df8d9-126">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="df8d9-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="df8d9-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="df8d9-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="df8d9-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="df8d9-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df8d9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="df8d9-129">Requirements</span></span>



| <span data-ttu-id="df8d9-130">需求</span><span class="sxs-lookup"><span data-stu-id="df8d9-130">Requirement</span></span> | <span data-ttu-id="df8d9-131">值</span><span class="sxs-lookup"><span data-stu-id="df8d9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df8d9-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df8d9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="df8d9-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df8d9-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="df8d9-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df8d9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="df8d9-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df8d9-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="df8d9-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="df8d9-136">End of client support</span></span><br/>    | <span data-ttu-id="df8d9-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="df8d9-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="df8d9-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="df8d9-138">End of server support</span></span><br/>    | <span data-ttu-id="df8d9-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df8d9-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="df8d9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df8d9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8d9-141">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="df8d9-141">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)
</dt> <dt>

[<span data-ttu-id="df8d9-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="df8d9-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
