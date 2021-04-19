---
description: 抓取列印伺服器上指定之印表機驅動程式套件的路徑。
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: 'GetPrinterDriverPackagePath 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987796"
---
# <a name="getprinterdriverpackagepath-function"></a><span data-ttu-id="27af1-103">GetPrinterDriverPackagePath 函式</span><span class="sxs-lookup"><span data-stu-id="27af1-103">GetPrinterDriverPackagePath function</span></span>

<span data-ttu-id="27af1-104">抓取列印伺服器上指定之印表機驅動程式套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="27af1-104">Retrieves the path to the specified printer driver package on a print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="27af1-105">語法</span><span class="sxs-lookup"><span data-stu-id="27af1-105">Syntax</span></span>


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a><span data-ttu-id="27af1-106">參數</span><span class="sxs-lookup"><span data-stu-id="27af1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27af1-107">*pszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27af1-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27af1-108">常數、以 null 結束的字串指標，指定列印伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="27af1-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="27af1-109">針對本機電腦使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="27af1-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="27af1-110">*pszEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27af1-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27af1-111">常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。</span><span class="sxs-lookup"><span data-stu-id="27af1-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="27af1-112">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27af1-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27af1-113">*pszLanguage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27af1-113">*pszLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27af1-114">常數、以 null 結束的字串指標，指定要安裝之驅動程式的 [多語系消費者介面](/windows/desktop/Intl/mui-resource-management) 語言。</span><span class="sxs-lookup"><span data-stu-id="27af1-114">A pointer to a constant, null-terminated string that specifies the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) language for the driver being installed.</span></span> <span data-ttu-id="27af1-115">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27af1-115">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27af1-116">*pszPackageID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27af1-116">*pszPackageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27af1-117">常數、以 null 結束的字串指標，指定驅動程式套件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27af1-117">A pointer to a constant, null-terminated string that specifies the ID of the driver package.</span></span>

</dd> <dt>

<span data-ttu-id="27af1-118">*pszDriverPackageCab* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="27af1-118">*pszDriverPackageCab* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="27af1-119">以 null 結束的字串指標，指定驅動程式套件的封包檔路徑。</span><span class="sxs-lookup"><span data-stu-id="27af1-119">A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package.</span></span> <span data-ttu-id="27af1-120">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27af1-120">This can be **NULL**.</span></span> <span data-ttu-id="27af1-121">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="27af1-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="27af1-122">*cchDriverPackageCab* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27af1-122">*cchDriverPackageCab* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27af1-123">*PszDriverPackageCab* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="27af1-123">The size, in characters, of the *pszDriverPackageCab* buffer.</span></span> <span data-ttu-id="27af1-124">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27af1-124">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27af1-125">*pcchRequiredSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="27af1-125">*pcchRequiredSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27af1-126">*PszDriverPackageCab* 緩衝區所需大小的指標。</span><span class="sxs-lookup"><span data-stu-id="27af1-126">A pointer to the required size of the *pszDriverPackageCab* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27af1-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="27af1-127">Return value</span></span>

<span data-ttu-id="27af1-128">如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="27af1-128">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="27af1-129">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="27af1-129">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="27af1-130">備註</span><span class="sxs-lookup"><span data-stu-id="27af1-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="27af1-131">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="27af1-131">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="27af1-132">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="27af1-132">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="27af1-133">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="27af1-133">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="27af1-134">若要取得 *cchDriverPackageCab* 的值，請使用 **Null** 做為 *pszDriverPackageCab* 的值來呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="27af1-134">To obtain a value for *cchDriverPackageCab*, call the function with **NULL** as the value of *pszDriverPackageCab*.</span></span> <span data-ttu-id="27af1-135">使用 *pcchRequiredSize* 中傳回的值做為 *cchDriverPackageCab* 的值，然後再次呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="27af1-135">Use the value returned in *pcchRequiredSize* as the value of *cchDriverPackageCab* and call the function again.</span></span>

<span data-ttu-id="27af1-136">*PszPackageID* 通常是從 [**GetCorePrinterDrivers**](getcoreprinterdrivers.md)的呼叫所取得。</span><span class="sxs-lookup"><span data-stu-id="27af1-136">The *pszPackageID* is typically obtained from a call to [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27af1-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="27af1-137">Requirements</span></span>



| <span data-ttu-id="27af1-138">需求</span><span class="sxs-lookup"><span data-stu-id="27af1-138">Requirement</span></span> | <span data-ttu-id="27af1-139">值</span><span class="sxs-lookup"><span data-stu-id="27af1-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27af1-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27af1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="27af1-141">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27af1-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="27af1-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27af1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="27af1-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27af1-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27af1-144">標頭</span><span class="sxs-lookup"><span data-stu-id="27af1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="27af1-145"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="27af1-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="27af1-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="27af1-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="27af1-147"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="27af1-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="27af1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="27af1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27af1-149"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27af1-149"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="27af1-150">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="27af1-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="27af1-151">**GetPrinterDriverPackagePathW** (Unicode) 和 **GetPrinterDriverPackagePathA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="27af1-151">**GetPrinterDriverPackagePathW** (Unicode) and **GetPrinterDriverPackagePathA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="27af1-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27af1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27af1-153">列印</span><span class="sxs-lookup"><span data-stu-id="27af1-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="27af1-154">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="27af1-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

