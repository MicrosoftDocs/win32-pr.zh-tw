---
description: 顯示對話方塊，讓使用者準備取得影像。
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: 'IWiaItem2：:D eviceDlg 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113313"
---
# <a name="iwiaitem2devicedlg-method"></a><span data-ttu-id="cdb9a-103">IWiaItem2：:D eviceDlg 方法</span><span class="sxs-lookup"><span data-stu-id="cdb9a-103">IWiaItem2::DeviceDlg method</span></span>

<span data-ttu-id="cdb9a-104">顯示對話方塊，讓使用者準備取得影像。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-104">Displays a dialog box to the user to prepare for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb9a-105">語法</span><span class="sxs-lookup"><span data-stu-id="cdb9a-105">Syntax</span></span>


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="cdb9a-106">參數</span><span class="sxs-lookup"><span data-stu-id="cdb9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb9a-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb9a-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="cdb9a-108">Type: **LONG**</span></span>

<span data-ttu-id="cdb9a-109">指定一組旗標來控制對話方塊的操作。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-109">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="cdb9a-110">值可以是0以代表預設行為，或 \_ \_ [**WiaFlag**](-wia-wiaflag.md)中所述的任何 WIA 裝置對話方塊旗標。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-110">The value can be either 0 to represent the default behavior or any of the WIA\_DEVICE\_DIALOG flags described in [**WiaFlag**](-wia-wiaflag.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdb9a-111">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb9a-112">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="cdb9a-112">Type: **HWND**</span></span>

<span data-ttu-id="cdb9a-113">父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-113">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="cdb9a-114">*bstrFolderName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-114">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb9a-115">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cdb9a-115">Type: **BSTR**</span></span>

<span data-ttu-id="cdb9a-116">指定要傳送檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-116">Specifies the folder name where the files are to be transferred.</span></span>

</dd> <dt>

<span data-ttu-id="cdb9a-117">*bstrFilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-117">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb9a-118">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cdb9a-118">Type: **BSTR**</span></span>

<span data-ttu-id="cdb9a-119">指定範本的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-119">Specifies the template file name.</span></span>

</dd> <dt>

<span data-ttu-id="cdb9a-120">*plNumFiles* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-120">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb9a-121">類型： \**LONG \** _</span><span class="sxs-lookup"><span data-stu-id="cdb9a-121">Type: \**LONG\** _</span></span>

<span data-ttu-id="cdb9a-122">_PpbstrFilePaths \* 陣列中專案數目的指標。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-122">A pointer to the number of items in the _ppbstrFilePaths\* array.</span></span>

</dd> <dt>

<span data-ttu-id="cdb9a-123">*ppbstrFilePaths* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-123">*ppbstrFilePaths* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb9a-124">類型： **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="cdb9a-124">Type: **BSTR\*\***</span></span>

<span data-ttu-id="cdb9a-125">掃描的檔案之路徑陣列的指標位址。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-125">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="cdb9a-126">在 IWiaItem2 之前，初始化指標以指向大小為零的陣列 (0) 0 **：呼叫:D evicedlg** 。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-126">Initialize the pointer to point to an array of size zero (0) before **IWiaItem2::DeviceDlg** is called.</span></span>

</dd> <dt>

<span data-ttu-id="cdb9a-127">*ppIWiaItem2* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-127">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb9a-128">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cdb9a-128">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="cdb9a-129">[**IWiaItem2**](-wia-iwiaitem2.md)介面指標陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-129">The address of an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdb9a-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdb9a-130">Return value</span></span>

<span data-ttu-id="cdb9a-131">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cdb9a-131">Type: **HRESULT**</span></span>

<span data-ttu-id="cdb9a-132">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-132">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cdb9a-133">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdb9a-134">備註</span><span class="sxs-lookup"><span data-stu-id="cdb9a-134">Remarks</span></span>

<span data-ttu-id="cdb9a-135">這個方法會向使用者顯示一個對話方塊，讓應用程式用來收集影像取得所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-135">This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition.</span></span> <span data-ttu-id="cdb9a-136">它也可用來指定影像掃描屬性，例如亮度和對比。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-136">It is also used to specify image scan properties such as brightness and contrast.</span></span>

<span data-ttu-id="cdb9a-137">在這個方法傳回之後，應用程式可以使用 [**IWiaTransfer**](-wia-iwiatransfer.md) 介面來取得影像。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-137">After this method returns, the application can use the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to acquire the image.</span></span>

<span data-ttu-id="cdb9a-138">應用程式必須針對它們透過 *ppIWiaItem2* 參數接收之介面指標陣列中的每個元素，呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-138">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method for each element in the array of interface pointers they receive through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="cdb9a-139">應用程式也必須使用 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)釋放陣列。</span><span class="sxs-lookup"><span data-stu-id="cdb9a-139">Applications must also free the array using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb9a-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdb9a-140">Requirements</span></span>



| <span data-ttu-id="cdb9a-141">需求</span><span class="sxs-lookup"><span data-stu-id="cdb9a-141">Requirement</span></span> | <span data-ttu-id="cdb9a-142">值</span><span class="sxs-lookup"><span data-stu-id="cdb9a-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb9a-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdb9a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb9a-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-144">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cdb9a-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdb9a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb9a-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdb9a-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cdb9a-147">標頭</span><span class="sxs-lookup"><span data-stu-id="cdb9a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdb9a-148"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="cdb9a-148"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdb9a-149">Idl</span><span class="sxs-lookup"><span data-stu-id="cdb9a-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdb9a-150"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdb9a-150"><dt>Wia.idl</dt></span></span> </dl> |



 

 
