---
description: ChangeDir 方法會將目前的智慧卡目錄變更為新指定的目錄。
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: ISCardFileAccess：： ChangeDir 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848046"
---
# <a name="iscardfileaccesschangedir-method"></a><span data-ttu-id="6cd3f-103">ISCardFileAccess：： ChangeDir 方法</span><span class="sxs-lookup"><span data-stu-id="6cd3f-103">ISCardFileAccess::ChangeDir method</span></span>

<span data-ttu-id="6cd3f-104">\[**ChangeDir** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-104">\[The **ChangeDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6cd3f-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6cd3f-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6cd3f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6cd3f-107">**ChangeDir** 方法會將目前的 [*智慧卡*](../secgloss/s-gly.md)目錄變更為新指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-107">The **ChangeDir** method changes the current [*smart card*](../secgloss/s-gly.md) directory to the new specified directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd3f-108">語法</span><span class="sxs-lookup"><span data-stu-id="6cd3f-108">Syntax</span></span>


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a><span data-ttu-id="6cd3f-109">參數</span><span class="sxs-lookup"><span data-stu-id="6cd3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd3f-110">*refType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6cd3f-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd3f-111">*BstrNewDir* 中使用的參考型別。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="6cd3f-112">**SC \_ 類型（ \_ 依 \_ 名稱）**</span><span class="sxs-lookup"><span data-stu-id="6cd3f-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="6cd3f-113">**SC \_ 類型（ \_ 依 \_ 識別碼）**</span><span class="sxs-lookup"><span data-stu-id="6cd3f-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="6cd3f-114">**SC \_ 類型 \_ （ \_ 簡短）**</span><span class="sxs-lookup"><span data-stu-id="6cd3f-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="6cd3f-115">**SC \_ 類型（ \_ 依 \_ 任何**</span><span class="sxs-lookup"><span data-stu-id="6cd3f-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="6cd3f-116">*bstrNewDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6cd3f-116">*bstrNewDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd3f-117">*RefType*) 要選取的檔案/目錄名稱 (。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-117">File/directory name (by *refType*) to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd3f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cd3f-118">Return value</span></span>

<span data-ttu-id="6cd3f-119">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6cd3f-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6cd3f-120">Return code</span></span>                                                                                   | <span data-ttu-id="6cd3f-121">Description</span><span class="sxs-lookup"><span data-stu-id="6cd3f-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6cd3f-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6cd3f-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6cd3f-123">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6cd3f-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6cd3f-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6cd3f-125">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6cd3f-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6cd3f-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6cd3f-127">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6cd3f-128">備註</span><span class="sxs-lookup"><span data-stu-id="6cd3f-128">Remarks</span></span>

<span data-ttu-id="6cd3f-129">若要取得目前所選目錄的絕對路徑，請呼叫 [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-129">To get an absolute path to the currently selected directory, call [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span></span>

<span data-ttu-id="6cd3f-130">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="6cd3f-131">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6cd3f-132">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd3f-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd3f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cd3f-133">Requirements</span></span>



| <span data-ttu-id="6cd3f-134">需求</span><span class="sxs-lookup"><span data-stu-id="6cd3f-134">Requirement</span></span> | <span data-ttu-id="6cd3f-135">值</span><span class="sxs-lookup"><span data-stu-id="6cd3f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6cd3f-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cd3f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd3f-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cd3f-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6cd3f-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cd3f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd3f-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cd3f-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6cd3f-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6cd3f-140">End of client support</span></span><br/>    | <span data-ttu-id="6cd3f-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6cd3f-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6cd3f-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6cd3f-142">End of server support</span></span><br/>    | <span data-ttu-id="6cd3f-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6cd3f-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6cd3f-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cd3f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd3f-145">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="6cd3f-145">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[<span data-ttu-id="6cd3f-146">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="6cd3f-146">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
