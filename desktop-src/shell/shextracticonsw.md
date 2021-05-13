---
description: 建立從指定檔案解壓縮之圖示的控制碼陣列。
title: SHExtractIconsW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840909"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="d343f-103">SHExtractIconsW 函式</span><span class="sxs-lookup"><span data-stu-id="d343f-103">SHExtractIconsW function</span></span>

<span data-ttu-id="d343f-104">\[**SHExtractIconsW** 可透過 Windows XP Service Pack 2 (SP2) 取得。</span><span class="sxs-lookup"><span data-stu-id="d343f-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="d343f-105">它可能會在後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d343f-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d343f-106">建立從指定檔案解壓縮之圖示的控制碼陣列。</span><span class="sxs-lookup"><span data-stu-id="d343f-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d343f-107">語法</span><span class="sxs-lookup"><span data-stu-id="d343f-107">Syntax</span></span>


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a><span data-ttu-id="d343f-108">參數</span><span class="sxs-lookup"><span data-stu-id="d343f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d343f-109">*>pszfilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d343f-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-110">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d343f-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d343f-111">要從中解壓縮圖示的檔案名指標。</span><span class="sxs-lookup"><span data-stu-id="d343f-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="d343f-112">*nIconIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d343f-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-113">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="d343f-113">Type: **int**</span></span>

<span data-ttu-id="d343f-114">要從名為 *>pszfilename* 之資源中解壓縮的第一個圖示索引。</span><span class="sxs-lookup"><span data-stu-id="d343f-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="d343f-115">*cxIcon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d343f-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-116">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="d343f-116">Type: **int**</span></span>

<span data-ttu-id="d343f-117">圖示所需的寬度。</span><span class="sxs-lookup"><span data-stu-id="d343f-117">The desired width of the icon.</span></span> <span data-ttu-id="d343f-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d343f-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d343f-119">*cyIcon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d343f-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-120">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="d343f-120">Type: **int**</span></span>

<span data-ttu-id="d343f-121">所需的圖示高度。</span><span class="sxs-lookup"><span data-stu-id="d343f-121">The desired height of the icon.</span></span> <span data-ttu-id="d343f-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d343f-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d343f-123">*phIcon* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d343f-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-124">類型： **HICON \***</span><span class="sxs-lookup"><span data-stu-id="d343f-124">Type: **HICON\***</span></span>

<span data-ttu-id="d343f-125">當此函式傳回時，會包含圖示控制碼陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d343f-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="d343f-126">*pIconId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d343f-126">*pIconId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-127">類型： **UINT \***</span><span class="sxs-lookup"><span data-stu-id="d343f-127">Type: **UINT\***</span></span>

<span data-ttu-id="d343f-128">當此函式傳回時，會包含最適合目前顯示裝置之已解壓縮圖示的資源識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="d343f-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="d343f-129">如果沒有適用于此格式的識別碼，則會包含0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="d343f-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="d343f-130">如果沒有任何其他原因可以取得任何識別碼，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d343f-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="d343f-131">*nIcons* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d343f-131">*nIcons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-132">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="d343f-132">Type: **UINT**</span></span>

<span data-ttu-id="d343f-133">要從名為 *>pszfilename* 的資源中解壓縮的圖示數目。</span><span class="sxs-lookup"><span data-stu-id="d343f-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="d343f-134">只有當資源是 .exe 或 .dll 檔案時，此參數才有效。</span><span class="sxs-lookup"><span data-stu-id="d343f-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="d343f-135">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d343f-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d343f-136">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="d343f-136">Type: **UINT**</span></span>

<span data-ttu-id="d343f-137">控制此函數的旗標。</span><span class="sxs-lookup"><span data-stu-id="d343f-137">The flags that control this function.</span></span> <span data-ttu-id="d343f-138">如需可能的值，請參閱 [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)函數的 *fuLoad* 參數。</span><span class="sxs-lookup"><span data-stu-id="d343f-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d343f-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="d343f-139">Return value</span></span>

<span data-ttu-id="d343f-140">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="d343f-140">Type: **UINT**</span></span>

<span data-ttu-id="d343f-141">如果成功，則為非零值;否則為零。</span><span class="sxs-lookup"><span data-stu-id="d343f-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d343f-142">備註</span><span class="sxs-lookup"><span data-stu-id="d343f-142">Remarks</span></span>

<span data-ttu-id="d343f-143">**SHExtractIconsW** 會從下列檔案類型中解壓縮。</span><span class="sxs-lookup"><span data-stu-id="d343f-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="d343f-144">可執行檔 (.exe)</span><span class="sxs-lookup"><span data-stu-id="d343f-144">Executable (.exe)</span></span>
-   <span data-ttu-id="d343f-145">DLL ( .dll) </span><span class="sxs-lookup"><span data-stu-id="d343f-145">DLL (.dll)</span></span>
-   <span data-ttu-id="d343f-146"> ( .ico) 圖示</span><span class="sxs-lookup"><span data-stu-id="d343f-146">Icon (.ico)</span></span>
-   <span data-ttu-id="d343f-147">資料指標 (。當前) </span><span class="sxs-lookup"><span data-stu-id="d343f-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="d343f-148"> ( 的動畫資料指標) </span><span class="sxs-lookup"><span data-stu-id="d343f-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="d343f-149">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="d343f-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="d343f-150">從 Windows 3 提取。也支援 *x* 16 位可執行檔 ( .exe 或 .dll) 。</span><span class="sxs-lookup"><span data-stu-id="d343f-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="d343f-151">*CxIcon* 和 *cyIcon* 參數指定要解壓縮的圖示大小。</span><span class="sxs-lookup"><span data-stu-id="d343f-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="d343f-152">您可以藉由在 LOWORD 和 HIWORD 之間分割值，在每個參數中解壓縮兩個大小。</span><span class="sxs-lookup"><span data-stu-id="d343f-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="d343f-153">將所需的第一個大小放在參數的 LOWORD 中，並將第二個大小放在 HIWORD 中。</span><span class="sxs-lookup"><span data-stu-id="d343f-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="d343f-154">例如， *cxIcon* 和 *cyIcon* 的 [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) (24，48) 會解壓縮24和48大小的圖示。</span><span class="sxs-lookup"><span data-stu-id="d343f-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="d343f-155">呼叫的進程會藉由呼叫 [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) 函式，負責終結透過此函式解壓縮的所有圖示。</span><span class="sxs-lookup"><span data-stu-id="d343f-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="d343f-156">**SHExtractIconsW** 不會依名稱匯出，也不會在公用標頭檔中宣告。</span><span class="sxs-lookup"><span data-stu-id="d343f-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="d343f-157">若要使用它，您必須宣告相符的原型，並使用 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來要求 Shell32.dll 的函式指標，而這些指標可以用來呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="d343f-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d343f-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="d343f-158">Requirements</span></span>



| <span data-ttu-id="d343f-159">需求</span><span class="sxs-lookup"><span data-stu-id="d343f-159">Requirement</span></span> | <span data-ttu-id="d343f-160">值</span><span class="sxs-lookup"><span data-stu-id="d343f-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d343f-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d343f-161">Minimum supported client</span></span><br/> | <span data-ttu-id="d343f-162">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d343f-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d343f-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d343f-163">Minimum supported server</span></span><br/> | <span data-ttu-id="d343f-164">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d343f-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d343f-165">DLL</span><span class="sxs-lookup"><span data-stu-id="d343f-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d343f-166"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d343f-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="d343f-167">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d343f-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d343f-168">**SHExtractIconsW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="d343f-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
