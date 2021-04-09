---
description: 目錄方法會從目前的目錄抓取指定類型的檔案清單。
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess：:D 目錄方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848756"
---
# <a name="iscardfileaccessdirectory-method"></a><span data-ttu-id="12c4d-103">ISCardFileAccess：:D 目錄方法</span><span class="sxs-lookup"><span data-stu-id="12c4d-103">ISCardFileAccess::Directory method</span></span>

<span data-ttu-id="12c4d-104">\[**目錄** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="12c4d-104">\[The **Directory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="12c4d-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="12c4d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="12c4d-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="12c4d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="12c4d-107">**目錄** 方法會從目前的目錄抓取指定類型的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="12c4d-107">The **Directory** method retrieves a list of files of the specified type from the current directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c4d-108">語法</span><span class="sxs-lookup"><span data-stu-id="12c4d-108">Syntax</span></span>


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a><span data-ttu-id="12c4d-109">參數</span><span class="sxs-lookup"><span data-stu-id="12c4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c4d-110">*類型類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12c4d-110">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c4d-111">要列出的 [*智慧卡*](../secgloss/s-gly.md) 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="12c4d-111">Type of [*smart card*](../secgloss/s-gly.md) files to list.</span></span>



| <span data-ttu-id="12c4d-112">值</span><span class="sxs-lookup"><span data-stu-id="12c4d-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="12c4d-113">意義</span><span class="sxs-lookup"><span data-stu-id="12c4d-113">Meaning</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <span data-ttu-id="12c4d-114"><dt>**SC \_ 類型 \_ 目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-114"><dt>**SC\_TYPE\_DIRECTORIES**</dt></span></span> </dl>           | <span data-ttu-id="12c4d-115">僅列出目錄檔。</span><span class="sxs-lookup"><span data-stu-id="12c4d-115">List directory files only.</span></span><br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <span data-ttu-id="12c4d-116"><dt>**SC \_ 類型 \_ 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-116"><dt>**SC\_TYPE\_FILES**</dt></span></span> </dl>                             | <span data-ttu-id="12c4d-117">僅列出基本檔案。</span><span class="sxs-lookup"><span data-stu-id="12c4d-117">List elementary files only.</span></span><br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <span data-ttu-id="12c4d-118"><dt>**SC \_ TYPE \_ ALL \_ FILES**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-118"><dt>**SC\_TYPE\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="12c4d-119">列出目錄和基本檔案。</span><span class="sxs-lookup"><span data-stu-id="12c4d-119">List both directory and elementary files.</span></span><br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <span data-ttu-id="12c4d-120"><dt>**SC \_ 類型 \_ 目錄 \_ 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-120"><dt>**SC\_TYPE\_DIRECTORY\_FILE**</dt></span></span> </dl> | <span data-ttu-id="12c4d-121">目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="12c4d-121">Directory file.</span></span><br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <span data-ttu-id="12c4d-122"><dt>**SC \_ 型別 \_ 透明 \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-122"><dt>**SC\_TYPE\_TRANSPARENT\_EF**</dt></span></span> </dl> | <span data-ttu-id="12c4d-123">透明的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="12c4d-123">Transparent elementary file.</span></span><br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <span data-ttu-id="12c4d-124"><dt>**SC \_ 類型 \_ 固定 \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-124"><dt>**SC\_TYPE\_FIXED\_EF**</dt></span></span> </dl>                   | <span data-ttu-id="12c4d-125">線性固定基本檔案。</span><span class="sxs-lookup"><span data-stu-id="12c4d-125">Linear fixed elementary file.</span></span><br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <span data-ttu-id="12c4d-126"><dt>**SC \_ 類型 \_ 迴圈 \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-126"><dt>**SC\_TYPE\_CYCLIC\_EF**</dt></span></span> </dl>                | <span data-ttu-id="12c4d-127">迴圈基本檔案。</span><span class="sxs-lookup"><span data-stu-id="12c4d-127">Cyclic elementary file.</span></span><br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <span data-ttu-id="12c4d-128"><dt>**SC \_ 類型 \_ 變數 \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-128"><dt>**SC\_TYPE\_VARIABLE\_EF**</dt></span></span> </dl>          | <span data-ttu-id="12c4d-129">線性變數基本檔案。</span><span class="sxs-lookup"><span data-stu-id="12c4d-129">Linear variable elementary file.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="12c4d-130">*ppFileList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="12c4d-130">*ppFileList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12c4d-131">Bstr 的陣列，代表符合檔 *類型* 中規範的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="12c4d-131">Array of BSTRs representing the list of files matching the specifier in *fileType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c4d-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="12c4d-132">Return value</span></span>

<span data-ttu-id="12c4d-133">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="12c4d-133">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="12c4d-134">傳回碼</span><span class="sxs-lookup"><span data-stu-id="12c4d-134">Return code</span></span>                                                                                   | <span data-ttu-id="12c4d-135">Description</span><span class="sxs-lookup"><span data-stu-id="12c4d-135">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="12c4d-136"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-136"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="12c4d-137">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="12c4d-137">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="12c4d-138"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-138"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="12c4d-139">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="12c4d-139">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="12c4d-140"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-140"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="12c4d-141">介面尚未執行此方法。</span><span class="sxs-lookup"><span data-stu-id="12c4d-141">The interface has not implemented this method.</span></span><br/> |
| <dl> <span data-ttu-id="12c4d-142"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-142"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="12c4d-143">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="12c4d-143">Out of memory.</span></span><br/>                                 |
| <dl> <span data-ttu-id="12c4d-144"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="12c4d-144"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="12c4d-145">傳入 *ppFileList* 的錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="12c4d-145">A bad pointer was passed in for *ppFileList*.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="12c4d-146">備註</span><span class="sxs-lookup"><span data-stu-id="12c4d-146">Remarks</span></span>

<span data-ttu-id="12c4d-147">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="12c4d-147">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="12c4d-148">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="12c4d-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="12c4d-149">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="12c4d-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12c4d-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="12c4d-150">Requirements</span></span>



| <span data-ttu-id="12c4d-151">需求</span><span class="sxs-lookup"><span data-stu-id="12c4d-151">Requirement</span></span> | <span data-ttu-id="12c4d-152">值</span><span class="sxs-lookup"><span data-stu-id="12c4d-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12c4d-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12c4d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="12c4d-154">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12c4d-154">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="12c4d-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12c4d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="12c4d-156">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12c4d-156">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="12c4d-157">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="12c4d-157">End of client support</span></span><br/>    | <span data-ttu-id="12c4d-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="12c4d-158">Windows XP</span></span><br/>                                |
| <span data-ttu-id="12c4d-159">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="12c4d-159">End of server support</span></span><br/>    | <span data-ttu-id="12c4d-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12c4d-160">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="12c4d-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12c4d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c4d-162">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="12c4d-162">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
