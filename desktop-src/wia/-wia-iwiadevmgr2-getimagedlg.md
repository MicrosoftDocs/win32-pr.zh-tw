---
description: IWiaDevMgr2：： GetImageDlg 方法會顯示一或多個對話方塊，讓使用者從 Windows 影像取得取得影像 (WIA) 2.0 裝置，並將該映射寫入指定的檔案。
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2：： GetImageDlg 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993147"
---
# <a name="iwiadevmgr2getimagedlg-method"></a><span data-ttu-id="7a191-103">IWiaDevMgr2：： GetImageDlg 方法</span><span class="sxs-lookup"><span data-stu-id="7a191-103">IWiaDevMgr2::GetImageDlg method</span></span>

<span data-ttu-id="7a191-104">**IWiaDevMgr2：： GetImageDlg** 方法會顯示一或多個對話方塊，讓使用者從 Windows 影像取得取得影像 (WIA) 2.0 裝置，並將該映射寫入指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="7a191-104">The **IWiaDevMgr2::GetImageDlg** method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="7a191-105">這個方法會擴充 [**IWiaDevMgr2：： SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) 的功能，以在單一 API 呼叫中封裝取得影像。</span><span class="sxs-lookup"><span data-stu-id="7a191-105">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a191-106">語法</span><span class="sxs-lookup"><span data-stu-id="7a191-106">Syntax</span></span>


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a><span data-ttu-id="7a191-107">參數</span><span class="sxs-lookup"><span data-stu-id="7a191-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a191-108">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a191-108">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-109">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="7a191-109">Type: **LONG**</span></span>

<span data-ttu-id="7a191-110">指定對話方塊的行為。</span><span class="sxs-lookup"><span data-stu-id="7a191-110">Specifies dialog box behavior.</span></span> <span data-ttu-id="7a191-111">可以設定為下列值：</span><span class="sxs-lookup"><span data-stu-id="7a191-111">Can be set to the following values:</span></span>



| <span data-ttu-id="7a191-112">旗標</span><span class="sxs-lookup"><span data-stu-id="7a191-112">Flag</span></span>                                 | <span data-ttu-id="7a191-113">意義</span><span class="sxs-lookup"><span data-stu-id="7a191-113">Meaning</span></span>                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a191-114">0</span><span class="sxs-lookup"><span data-stu-id="7a191-114">0</span></span>                                    | <span data-ttu-id="7a191-115">預設行為。</span><span class="sxs-lookup"><span data-stu-id="7a191-115">Default behavior.</span></span>                                                                                                                                                           |
| <span data-ttu-id="7a191-116">WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI</span><span class="sxs-lookup"><span data-stu-id="7a191-116">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="7a191-117">使用系統 UI，而不是廠商提供的 UI。</span><span class="sxs-lookup"><span data-stu-id="7a191-117">Use the system UI instead of the vendor-supplied UI.</span></span> <span data-ttu-id="7a191-118">如果系統 UI 無法使用，則會使用廠商 UI。</span><span class="sxs-lookup"><span data-stu-id="7a191-118">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="7a191-119">如果沒有可用的 UI，函數會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="7a191-119">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7a191-120">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a191-120">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-121">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a191-121">Type: **BSTR**</span></span>

<span data-ttu-id="7a191-122">指定要使用的掃描器。</span><span class="sxs-lookup"><span data-stu-id="7a191-122">Specifies the scanner to use.</span></span>

</dd> <dt>

<span data-ttu-id="7a191-123">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a191-123">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-124">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="7a191-124">Type: **HWND**</span></span>

<span data-ttu-id="7a191-125">擁有 [ **取得影像** ] 對話方塊的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="7a191-125">A handle of the window that owns the **Get Image** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="7a191-126">*bstrFolderName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a191-126">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-127">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a191-127">Type: **BSTR**</span></span>

<span data-ttu-id="7a191-128">指定儲存掃描之檔案的分成資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="7a191-128">Specifies the name of the folder ito store the scanned files in.</span></span>

</dd> <dt>

<span data-ttu-id="7a191-129">*bstrFilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a191-129">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-130">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a191-130">Type: **BSTR**</span></span>

<span data-ttu-id="7a191-131">指定要寫入影像資料的檔案名。</span><span class="sxs-lookup"><span data-stu-id="7a191-131">Specifies the name of the file to write the image data to.</span></span>

</dd> <dt>

<span data-ttu-id="7a191-132">*plNumFiles* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a191-132">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-133">類型： \**LONG \** _</span><span class="sxs-lookup"><span data-stu-id="7a191-133">Type: \**LONG\** _</span></span>

<span data-ttu-id="7a191-134">要掃描的檔數目指標。</span><span class="sxs-lookup"><span data-stu-id="7a191-134">A pointer to the number of files to scan.</span></span>

</dd> <dt>

<span data-ttu-id="7a191-135">_ppbstrFilePaths \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a191-135">_ppbstrFilePaths\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-136">類型： **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="7a191-136">Type: **BSTR\*\***</span></span>

<span data-ttu-id="7a191-137">掃描的檔案之路徑陣列的指標位址。</span><span class="sxs-lookup"><span data-stu-id="7a191-137">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="7a191-138">在呼叫 **IWiaDevMgr2：： GetImageDlg** 之前，初始化指標以指向大小為零的陣列 (0) 。</span><span class="sxs-lookup"><span data-stu-id="7a191-138">Initialize the pointer to point to an array of size zero (0) before **IWiaDevMgr2::GetImageDlg** is called.</span></span> <span data-ttu-id="7a191-139">請參閱 **備註**。</span><span class="sxs-lookup"><span data-stu-id="7a191-139">See **Remarks**.</span></span>

</dd> <dt>

<span data-ttu-id="7a191-140">*ppItem* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7a191-140">*ppItem* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a191-141">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7a191-141">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="7a191-142">[**IWiaItem2**](-wia-iwiaitem2.md)影像掃描來源之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="7a191-142">The address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) that the images were scanned from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a191-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a191-143">Return value</span></span>

<span data-ttu-id="7a191-144">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7a191-144">Type: **HRESULT**</span></span>

<span data-ttu-id="7a191-145">如果資料傳輸成功， **IWiaDevMgr2：： GetImageDlg** 會 \_ 傳回 s OK， \_ 如果使用者取消對話方塊，則傳回 FALSE，否則會傳回標準 COM 錯誤。</span><span class="sxs-lookup"><span data-stu-id="7a191-145">**IWiaDevMgr2::GetImageDlg** returns S\_OK if the data is transferred successfully, returns S\_FALSE if the user cancels the dialog box, or returns a standard COM error.</span></span>

> [!Note]  
> <span data-ttu-id="7a191-146">如果函數傳回 FALSE，則 *ppbstrFilePaths* 參數不一定是空的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7a191-146">The *ppbstrFilePaths* parameter is not necessarily empty, if the function returns S\_FALSE.</span></span> <span data-ttu-id="7a191-147">如果使用者取消，則會處理已完成掃描的頁面，並在 *ppbstrFilePaths* 中傳回。</span><span class="sxs-lookup"><span data-stu-id="7a191-147">If the user cancels, the pages that have completed scanning are processed and returned in *ppbstrFilePaths*.</span></span> <span data-ttu-id="7a191-148">即使未使用它們，您也必須釋放陣列。</span><span class="sxs-lookup"><span data-stu-id="7a191-148">Even if they are not used, you must free the array.</span></span> <span data-ttu-id="7a191-149">請參閱 **備註**。</span><span class="sxs-lookup"><span data-stu-id="7a191-149">See **Remarks**.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="7a191-150">備註</span><span class="sxs-lookup"><span data-stu-id="7a191-150">Remarks</span></span>

<span data-ttu-id="7a191-151">如果應用程式傳遞 **Null** 作為 *bstrDeviceID* 參數的值， **IWiaDevMgr2：： GetImageDlg** 會顯示 [ **選取裝置** ] 對話方塊，讓使用者可以選取 WIA 2.0 輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="7a191-151">If the application passes **NULL** for the value of the *bstrDeviceID* parameter, **IWiaDevMgr2::GetImageDlg** displays the **Select Device** dialog box so that the user can select the WIA 2.0 input device.</span></span>

<span data-ttu-id="7a191-152">**在 [檔案**] 功能表上使用以 [**掃描器**] 命名的功能表項目，讓您的應用程式可以使用裝置和映射選取專案。</span><span class="sxs-lookup"><span data-stu-id="7a191-152">Use a menu item named **From scanner** on the **File** menu so that device and image selections are available in your application.</span></span>

<span data-ttu-id="7a191-153">在 *ppbstrFilePaths* 指向的陣列中的每個 BSTR 上呼叫 [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) \[ \] ，然後在陣列本身呼叫 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) ，以釋放相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7a191-153">Call [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) on each BSTR in the array that *ppbstrFilePaths*\[i\] points to, and call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) on the array itself to free associated memory.</span></span> <span data-ttu-id="7a191-154">如果 \_ 傳回 FALSE，請檢查 *plNumFiles* 指向的值是否不是零。</span><span class="sxs-lookup"><span data-stu-id="7a191-154">If S\_FALSE is returned, check to see if the value that *plNumFiles* points to is not zero.</span></span> <span data-ttu-id="7a191-155">如果此值不是零，則 \[ \] 會在應用程式中釋放 ppbstrFilePaths i 的資源，因為使用者可能會在掃描一或多個頁面之後取消。</span><span class="sxs-lookup"><span data-stu-id="7a191-155">If the value is not zero, free the *ppbstrFilePaths*\[i\] resources in the application, because the user might cancel after scanning one or more pages.</span></span> <span data-ttu-id="7a191-156">在呼叫 **IWiaDevMgr2：： GetImageDlg** 之前，將 *plNumFiles* 初始化為零。</span><span class="sxs-lookup"><span data-stu-id="7a191-156">Initialize *plNumFiles* to zero before you call **IWiaDevMgr2::GetImageDlg**.</span></span> <span data-ttu-id="7a191-157">如果 *plNumFiles* 未初始化為零，而且 COM 基礎結構中的失敗導致函式在 \_ 呼叫 **IWiaDevMgr2：： GetImageDlg** 之前傳回 FALSE，則 *plNumFiles* 會有誤導的垃圾值。</span><span class="sxs-lookup"><span data-stu-id="7a191-157">If *plNumFiles* is not initialized to zero and a failure in the COM infrastructure causes the function to return S\_FALSE before **IWiaDevMgr2::GetImageDlg** is called, then *plNumFiles* will have a misleading garbage value.</span></span>

<span data-ttu-id="7a191-158">對話方塊必須有足夠的許可權可以 *bstrFolderName* ，以便儲存具有唯一檔案名的檔案。</span><span class="sxs-lookup"><span data-stu-id="7a191-158">The dialog box must have sufficient rights to *bstrFolderName* so that it can save the files with unique file names.</span></span> <span data-ttu-id="7a191-159">使用存取控制清單來保護資料夾 (ACL) ，因為它包含使用者資料。</span><span class="sxs-lookup"><span data-stu-id="7a191-159">Protect the folder with an access control list (ACL) because it contains user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a191-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a191-160">Requirements</span></span>



| <span data-ttu-id="7a191-161">需求</span><span class="sxs-lookup"><span data-stu-id="7a191-161">Requirement</span></span> | <span data-ttu-id="7a191-162">值</span><span class="sxs-lookup"><span data-stu-id="7a191-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7a191-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a191-163">Minimum supported client</span></span><br/> | <span data-ttu-id="7a191-164">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a191-164">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7a191-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a191-165">Minimum supported server</span></span><br/> | <span data-ttu-id="7a191-166">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a191-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7a191-167">標頭</span><span class="sxs-lookup"><span data-stu-id="7a191-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a191-168"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="7a191-168"><dt>Wia.h</dt></span></span> </dl> |



 

 
