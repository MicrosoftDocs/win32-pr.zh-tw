---
description: FindMediaFile 方法會搜尋檔案，如果成功，則會抓取檔案的路徑。
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'IMediaLocator：： FindMediaFile 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983974"
---
# <a name="imedialocatorfindmediafile-method"></a><span data-ttu-id="61ace-103">IMediaLocator：： FindMediaFile 方法</span><span class="sxs-lookup"><span data-stu-id="61ace-103">IMediaLocator::FindMediaFile method</span></span>

> [!Note]  
> <span data-ttu-id="61ace-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="61ace-104">\[Deprecated.</span></span> <span data-ttu-id="61ace-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="61ace-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="61ace-106">方法會搜尋檔案，如果成功，則會抓取檔案 `FindMediaFile` 的路徑。</span><span class="sxs-lookup"><span data-stu-id="61ace-106">The `FindMediaFile` method searches for a file and, if successful, retrieves the path to the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ace-107">語法</span><span class="sxs-lookup"><span data-stu-id="61ace-107">Syntax</span></span>


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a><span data-ttu-id="61ace-108">參數</span><span class="sxs-lookup"><span data-stu-id="61ace-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ace-109">*輸入*</span><span class="sxs-lookup"><span data-stu-id="61ace-109">*Input*</span></span> 
</dt> <dd>

<span data-ttu-id="61ace-110">檔案名，包括路徑，也就是最後已知的檔案所在的路徑。</span><span class="sxs-lookup"><span data-stu-id="61ace-110">File name, including path, where the file was last known to reside.</span></span> <span data-ttu-id="61ace-111">若為時間軸中的來源物件，請使用目前的媒體名稱。</span><span class="sxs-lookup"><span data-stu-id="61ace-111">For source objects in the timeline, use the current media name.</span></span>

</dd> <dt>

<span data-ttu-id="61ace-112">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="61ace-112">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="61ace-113">包含篩選字串配對的 **BSTR** ，格式為 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrFilter** 成員所需。</span><span class="sxs-lookup"><span data-stu-id="61ace-113">A **BSTR** containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="61ace-114">如果媒體定位器顯示 [開啟檔案] 對話方塊，則會使用此篩選器。</span><span class="sxs-lookup"><span data-stu-id="61ace-114">The media locator uses this filter if it displays a File Open dialog box.</span></span> <span data-ttu-id="61ace-115">如果 Flags 參數未包含 SFN VALIDATEF 快顯旗 *標*，則此值可以是 **Null** \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="61ace-115">The value can be **NULL** if the *Flags* parameter does not include the SFN\_VALIDATEF\_POPUP flag.</span></span>

</dd> <dt>

<span data-ttu-id="61ace-116">*pOutput*</span><span class="sxs-lookup"><span data-stu-id="61ace-116">*pOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="61ace-117">如果變數與 *輸入* 中包含的值不同，而且方法成功找到檔案，則為收到檔案實際路徑的變數指標。</span><span class="sxs-lookup"><span data-stu-id="61ace-117">Pointer to a variable that receives the actual path to the file, if it differs from the value contained in *Input* and if the method successfully locates the file.</span></span>

</dd> <dt>

<span data-ttu-id="61ace-118">*旗標*</span><span class="sxs-lookup"><span data-stu-id="61ace-118">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="61ace-119">零或多個旗標的位元組合。</span><span class="sxs-lookup"><span data-stu-id="61ace-119">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="61ace-120">如需可能旗標的清單，請參閱 [**檔案名驗證旗標**](file-name-validation-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="61ace-120">For a list of possible flags, see [**File Name Validation Flags**](file-name-validation-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61ace-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="61ace-121">Return value</span></span>

<span data-ttu-id="61ace-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="61ace-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61ace-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61ace-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61ace-124">備註</span><span class="sxs-lookup"><span data-stu-id="61ace-124">Remarks</span></span>

<span data-ttu-id="61ace-125">[開啟檔案] 對話方塊的篩選字串（由 *FilterString* 參數指定）包含內部 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="61ace-125">The filter string for the File Open dialog, which is specified by the *FilterString* parameter, contains internal Null characters.</span></span> <span data-ttu-id="61ace-126">例如，Video \\ 0 \* . avi \\ 0 \\ 0 是有效的篩選字串。</span><span class="sxs-lookup"><span data-stu-id="61ace-126">For example, Video\\0\*.avi\\0\\0 is a valid filter string.</span></span> <span data-ttu-id="61ace-127">您無法使用 **SysAllocStr** 函式來配置 BSTR，因為該函式需要以 null 終止的字串，且會在第一個 Null 字元截斷字串。</span><span class="sxs-lookup"><span data-stu-id="61ace-127">You cannot use the **SysAllocStr** function to allocate the BSTR, because that function expects a Null-terminated string and will truncate the string at the first Null character.</span></span> <span data-ttu-id="61ace-128">因此，請使用類似 **SysAllocStringLen** 的函式，其中包含長度的明確參數：</span><span class="sxs-lookup"><span data-stu-id="61ace-128">Therefore, use a function such as **SysAllocStringLen**, which includes an explicit parameter for the length:</span></span>


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



<span data-ttu-id="61ace-129">如果使用者取消 [開啟檔案] 對話方塊，方法會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="61ace-129">If the user cancels the File Open dialog, the method returns E\_FAIL.</span></span>

<span data-ttu-id="61ace-130">方法會為 *pOutput* 中的 **BSTR** 配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="61ace-130">The method allocates memory for the **BSTR** in *pOutput*.</span></span> <span data-ttu-id="61ace-131">應用程式必須呼叫 **SysFreeString** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="61ace-131">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="61ace-132">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="61ace-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="61ace-133">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="61ace-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="61ace-134">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="61ace-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61ace-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="61ace-135">Requirements</span></span>



| <span data-ttu-id="61ace-136">需求</span><span class="sxs-lookup"><span data-stu-id="61ace-136">Requirement</span></span> | <span data-ttu-id="61ace-137">值</span><span class="sxs-lookup"><span data-stu-id="61ace-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61ace-138">標頭</span><span class="sxs-lookup"><span data-stu-id="61ace-138">Header</span></span><br/>  | <dl> <span data-ttu-id="61ace-139"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="61ace-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="61ace-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="61ace-140">Library</span></span><br/> | <dl> <span data-ttu-id="61ace-141"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61ace-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61ace-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61ace-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ace-143">**IMediaLocator 介面**</span><span class="sxs-lookup"><span data-stu-id="61ace-143">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="61ace-144">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="61ace-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
