---
description: 估計在指定檔案上呼叫處理常式時，執行未知程式碼的風險。 此風險是以瞭解處理常式和檔案的程式碼內容為基礎。
title: EstimateFileRiskLevel 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 96798e0bc64b39ae7f18d58b97fafafc9dc2508b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973616"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="6a294-104">EstimateFileRiskLevel 函式</span><span class="sxs-lookup"><span data-stu-id="6a294-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="6a294-105">\[這項功能可在 Windows XP Service Pack 2 (SP2) 到 Windows Vista 中使用。</span><span class="sxs-lookup"><span data-stu-id="6a294-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="6a294-106">它可能會在後續版本的 Windows 中改變或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6a294-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="6a294-107">用戶端應用程式應該改用 [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) 來呈現可透過電子郵件和郵件附件安全地下載和交換檔案的使用者環境。\]</span><span class="sxs-lookup"><span data-stu-id="6a294-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="6a294-108">估計在指定檔案上呼叫處理常式時，執行未知程式碼的風險。</span><span class="sxs-lookup"><span data-stu-id="6a294-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="6a294-109">此風險是以瞭解處理常式和檔案的程式碼內容為基礎。</span><span class="sxs-lookup"><span data-stu-id="6a294-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a294-110">語法</span><span class="sxs-lookup"><span data-stu-id="6a294-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="6a294-111">參數</span><span class="sxs-lookup"><span data-stu-id="6a294-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a294-112">*pszFilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a294-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a294-113">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6a294-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="6a294-114">以 null 結束的字串指標，其中包含針對處理常式所檢查之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="6a294-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="6a294-115">*pszExt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a294-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a294-116">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6a294-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="6a294-117">以 null 結束的字串指標，其中包含所檢查之檔案的副檔名（不論是否有前置句點）。</span><span class="sxs-lookup"><span data-stu-id="6a294-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="6a294-118">例如，「.txt」或「txt」。</span><span class="sxs-lookup"><span data-stu-id="6a294-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="6a294-119">*pszHandler* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a294-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a294-120">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6a294-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="6a294-121">以 null 結束的字串指標，其中包含檔案處理常式的路徑。</span><span class="sxs-lookup"><span data-stu-id="6a294-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="6a294-122">*pfrlEstimate* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6a294-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a294-123">類型： \**檔 \_ 風險 \_ 層 \* 級* _</span><span class="sxs-lookup"><span data-stu-id="6a294-123">Type: \**FILE\_RISK\_LEVEL\** _</span></span>

<span data-ttu-id="6a294-124">當此函式成功傳回時，會包含下列其中一個值的指標，以指出預估的風險。</span><span class="sxs-lookup"><span data-stu-id="6a294-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="6a294-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL \_ 沒有任何 \_ 意見*\* (0) </span><span class="sxs-lookup"><span data-stu-id="6a294-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL\_NO\_OPINION*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="6a294-126">找不到檔案格式或未識別處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a294-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="6a294-127">沒有足夠的資訊可提供有意義的答案。</span><span class="sxs-lookup"><span data-stu-id="6a294-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="6a294-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_低** (1) </span><span class="sxs-lookup"><span data-stu-id="6a294-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a294-129">檔案的格式已完全瞭解、已知處理常式，而且不會執行任何多餘的程式碼。</span><span class="sxs-lookup"><span data-stu-id="6a294-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="6a294-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_適中** (2) </span><span class="sxs-lookup"><span data-stu-id="6a294-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a294-131">已識別檔案的格式，但無法充分瞭解將其標示為高或低風險。</span><span class="sxs-lookup"><span data-stu-id="6a294-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="6a294-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_高** (3) </span><span class="sxs-lookup"><span data-stu-id="6a294-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6a294-133">您可以瞭解檔案格式，並已識別出更高的風險因素。</span><span class="sxs-lookup"><span data-stu-id="6a294-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="6a294-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_封鎖** (4) </span><span class="sxs-lookup"><span data-stu-id="6a294-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6a294-135">此處理程式會特別封鎖檔案格式。</span><span class="sxs-lookup"><span data-stu-id="6a294-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a294-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a294-136">Return value</span></span>

<span data-ttu-id="6a294-137">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a294-137">Type: **HRESULT**</span></span>

<span data-ttu-id="6a294-138">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6a294-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a294-139">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6a294-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a294-140">備註</span><span class="sxs-lookup"><span data-stu-id="6a294-140">Remarks</span></span>

<span data-ttu-id="6a294-141">此函式未在公用標頭中宣告，或包含在程式庫檔案中。</span><span class="sxs-lookup"><span data-stu-id="6a294-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="6a294-142">若要使用它，您必須將它直接從 Winshfhc.dll 由序數101載入。</span><span class="sxs-lookup"><span data-stu-id="6a294-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a294-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a294-143">Requirements</span></span>



| <span data-ttu-id="6a294-144">需求</span><span class="sxs-lookup"><span data-stu-id="6a294-144">Requirement</span></span> | <span data-ttu-id="6a294-145">值</span><span class="sxs-lookup"><span data-stu-id="6a294-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a294-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a294-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6a294-147">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a294-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6a294-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a294-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6a294-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a294-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6a294-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6a294-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a294-151"><dt>Winshfhc.dll (5.1 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6a294-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




