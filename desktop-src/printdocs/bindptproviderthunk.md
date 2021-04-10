---
description: 開啟列印票證提供者的實例。
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192608"
---
# <a name="bindptproviderthunk-function"></a><span data-ttu-id="226c2-103">BindPTProviderThunk 函式</span><span class="sxs-lookup"><span data-stu-id="226c2-103">BindPTProviderThunk function</span></span>

<span data-ttu-id="226c2-104">\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。</span><span class="sxs-lookup"><span data-stu-id="226c2-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="226c2-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) 會提供對等的功能，因此應該改用。\]</span><span class="sxs-lookup"><span data-stu-id="226c2-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="226c2-106">開啟列印票證提供者的實例。</span><span class="sxs-lookup"><span data-stu-id="226c2-106">Opens an instance of a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="226c2-107">語法</span><span class="sxs-lookup"><span data-stu-id="226c2-107">Syntax</span></span>


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a><span data-ttu-id="226c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="226c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="226c2-109">*pszPrinterName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="226c2-109">*pszPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="226c2-110">列印佇列的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="226c2-110">The full name of a print queue.</span></span>

</dd> <dt>

<span data-ttu-id="226c2-111">*odata-maxversion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="226c2-111">*maxVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="226c2-112">呼叫端所支援的最新 [列印架構](./printschema.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="226c2-112">The latest version of the [Print Schema](./printschema.md) that the caller supports.</span></span>

</dd> <dt>

<span data-ttu-id="226c2-113">*prefVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="226c2-113">*prefVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="226c2-114">呼叫端所要求的 [列印架構](./printschema.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="226c2-114">The version of the [Print Schema](./printschema.md) requested by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="226c2-115">*phProvider* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="226c2-115">*phProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="226c2-116">指向列印票證提供者之控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="226c2-116">A pointer to a handle to the print ticket provider.</span></span>

</dd> <dt>

<span data-ttu-id="226c2-117">*usedVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="226c2-117">*usedVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="226c2-118">列印票證提供者將使用的 [列印架構](./printschema.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="226c2-118">The version of the [Print Schema](./printschema.md) that the print ticket provider will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="226c2-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="226c2-119">Return value</span></span>

<span data-ttu-id="226c2-120">如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="226c2-120">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="226c2-121">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="226c2-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="226c2-122">備註</span><span class="sxs-lookup"><span data-stu-id="226c2-122">Remarks</span></span>

<span data-ttu-id="226c2-123">呼叫此函式之前，呼叫的執行緒必須呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)來初始化 COM。</span><span class="sxs-lookup"><span data-stu-id="226c2-123">Before calling this function, the calling thread must initialize COM by calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

## <a name="requirements"></a><span data-ttu-id="226c2-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="226c2-124">Requirements</span></span>



| <span data-ttu-id="226c2-125">需求</span><span class="sxs-lookup"><span data-stu-id="226c2-125">Requirement</span></span> | <span data-ttu-id="226c2-126">值</span><span class="sxs-lookup"><span data-stu-id="226c2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="226c2-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="226c2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="226c2-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="226c2-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="226c2-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="226c2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="226c2-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="226c2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="226c2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="226c2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="226c2-132"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="226c2-132"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="226c2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="226c2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226c2-134">列印架構</span><span class="sxs-lookup"><span data-stu-id="226c2-134">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="226c2-135">**PTOpenProviderEx**</span><span class="sxs-lookup"><span data-stu-id="226c2-135">**PTOpenProviderEx**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[<span data-ttu-id="226c2-136">列印</span><span class="sxs-lookup"><span data-stu-id="226c2-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="226c2-137">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="226c2-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

