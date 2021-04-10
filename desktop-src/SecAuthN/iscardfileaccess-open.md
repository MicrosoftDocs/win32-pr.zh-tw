---
description: Open 方法會開啟指定的檔案，以供進一步使用。
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: ISCardFileAccess：： Open 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115340"
---
# <a name="iscardfileaccessopen-method"></a><span data-ttu-id="c4fc7-103">ISCardFileAccess：： Open 方法</span><span class="sxs-lookup"><span data-stu-id="c4fc7-103">ISCardFileAccess::Open method</span></span>

<span data-ttu-id="c4fc7-104">\[**Open** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c4fc7-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c4fc7-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c4fc7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c4fc7-107">**Open** 方法會開啟指定的檔案，以供進一步使用。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-107">The **Open** method opens the specified file for further use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4fc7-108">語法</span><span class="sxs-lookup"><span data-stu-id="c4fc7-108">Syntax</span></span>


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a><span data-ttu-id="c4fc7-109">參數</span><span class="sxs-lookup"><span data-stu-id="c4fc7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4fc7-110">*refType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4fc7-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fc7-111">*BstrPathSpec* 中使用的參考型別。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="c4fc7-112">**SC \_ 類型（ \_ 依 \_ 名稱）**</span><span class="sxs-lookup"><span data-stu-id="c4fc7-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="c4fc7-113">**SC \_ 類型（ \_ 依 \_ 識別碼）**</span><span class="sxs-lookup"><span data-stu-id="c4fc7-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="c4fc7-114">**SC \_ 類型 \_ （ \_ 簡短）**</span><span class="sxs-lookup"><span data-stu-id="c4fc7-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="c4fc7-115">**SC \_ 類型（ \_ 依 \_ 任何**</span><span class="sxs-lookup"><span data-stu-id="c4fc7-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="c4fc7-116">*bstrPathSpec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4fc7-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fc7-117">要開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-117">File to open.</span></span>

</dd> <dt>

<span data-ttu-id="c4fc7-118">*phFile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c4fc7-118">*phFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fc7-119">\_將保存檔案控制代碼之 HSCARD 檔的指標。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-119">Pointer to an HSCARD\_FILE that will hold the file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4fc7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4fc7-120">Return value</span></span>

<span data-ttu-id="c4fc7-121">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c4fc7-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c4fc7-122">Return code</span></span>                                                                                   | <span data-ttu-id="c4fc7-123">Description</span><span class="sxs-lookup"><span data-stu-id="c4fc7-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c4fc7-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c4fc7-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c4fc7-125">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c4fc7-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c4fc7-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c4fc7-127">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="c4fc7-128"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c4fc7-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c4fc7-129">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="c4fc7-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c4fc7-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c4fc7-131">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c4fc7-132">備註</span><span class="sxs-lookup"><span data-stu-id="c4fc7-132">Remarks</span></span>

<span data-ttu-id="c4fc7-133">若要關閉檔案，請呼叫 [**close**](iscardfileaccess-close.md)。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-133">To close a file, call [**Close**](iscardfileaccess-close.md).</span></span>

<span data-ttu-id="c4fc7-134">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="c4fc7-135">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c4fc7-136">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="c4fc7-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4fc7-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4fc7-137">Requirements</span></span>



| <span data-ttu-id="c4fc7-138">需求</span><span class="sxs-lookup"><span data-stu-id="c4fc7-138">Requirement</span></span> | <span data-ttu-id="c4fc7-139">值</span><span class="sxs-lookup"><span data-stu-id="c4fc7-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c4fc7-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4fc7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c4fc7-141">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4fc7-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c4fc7-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4fc7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c4fc7-143">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4fc7-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c4fc7-144">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c4fc7-144">End of client support</span></span><br/>    | <span data-ttu-id="c4fc7-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c4fc7-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c4fc7-146">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c4fc7-146">End of server support</span></span><br/>    | <span data-ttu-id="c4fc7-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4fc7-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c4fc7-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4fc7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4fc7-149">**關閉**</span><span class="sxs-lookup"><span data-stu-id="c4fc7-149">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-150">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="c4fc7-150">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
