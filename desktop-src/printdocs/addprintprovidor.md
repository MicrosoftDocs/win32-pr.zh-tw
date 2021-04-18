---
description: AddPrintProvidor 函式會安裝本機列印提供者，並連結設定、資料和提供者檔案。
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: 'AddPrintProvidor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989385"
---
# <a name="addprintprovidor-function"></a><span data-ttu-id="d9d49-103">AddPrintProvidor 函式</span><span class="sxs-lookup"><span data-stu-id="d9d49-103">AddPrintProvidor function</span></span>

<span data-ttu-id="d9d49-104">**AddPrintProvidor** 函式會安裝本機列印提供者，並連結設定、資料和提供者檔案。</span><span class="sxs-lookup"><span data-stu-id="d9d49-104">The **AddPrintProvidor** function installs a local print provider and links the configuration, data, and provider files.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d49-105">語法</span><span class="sxs-lookup"><span data-stu-id="d9d49-105">Syntax</span></span>


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d9d49-106">參數</span><span class="sxs-lookup"><span data-stu-id="d9d49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9d49-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9d49-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d49-108">以 null 結束的字串指標，指定應該安裝提供者之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9d49-108">A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed.</span></span> <span data-ttu-id="d9d49-109">針對僅支援提供者本機安裝的系統，此參數應為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d9d49-109">For systems that only support local installation of providers, this parameter should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d9d49-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9d49-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d49-111">*PProviderInfo* 所指向之結構的層級。</span><span class="sxs-lookup"><span data-stu-id="d9d49-111">The level of the structure to which *pProviderInfo* points.</span></span> <span data-ttu-id="d9d49-112">它可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="d9d49-112">It can be one of the following.</span></span>



| <span data-ttu-id="d9d49-113">值</span><span class="sxs-lookup"><span data-stu-id="d9d49-113">Value</span></span>                                                                                                | <span data-ttu-id="d9d49-114">意義</span><span class="sxs-lookup"><span data-stu-id="d9d49-114">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d9d49-115"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d9d49-115"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d9d49-116">函數會使用 [**PROVIDOR \_ INFO \_ 1**](providor-info-1.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d9d49-116">Function uses a [**PROVIDOR\_INFO\_1**](providor-info-1.md) structure.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="d9d49-117"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d9d49-117"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d9d49-118">函數會使用 [**PROVIDOR \_ INFO \_ 2**](providor-info-2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d9d49-118">Function uses a [**PROVIDOR\_INFO\_2**](providor-info-2.md) structure.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9d49-119">*pProviderInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9d49-119">*pProviderInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d49-120">列印提供者結構的指標，由 *層級* 表示。</span><span class="sxs-lookup"><span data-stu-id="d9d49-120">A pointer to a print provider structure, as indicated by *Level*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9d49-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9d49-121">Return value</span></span>

<span data-ttu-id="d9d49-122">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="d9d49-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d9d49-123">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="d9d49-123">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d49-124">備註</span><span class="sxs-lookup"><span data-stu-id="d9d49-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d9d49-125">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="d9d49-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d9d49-126">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="d9d49-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d9d49-127">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="d9d49-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d9d49-128">在應用程式呼叫 **AddPrintProvidor** 函式之前，提供者所需的所有檔案都必須複製到 SYSTEM32 目錄。</span><span class="sxs-lookup"><span data-stu-id="d9d49-128">Before an application calls the **AddPrintProvidor** function, all files required by the provider must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="d9d49-129">藉由呼叫 [**DeletePrintProvidor**](deleteprintprovidor.md)，可移除 **AddPrintProvidor** 所新增的提供者。</span><span class="sxs-lookup"><span data-stu-id="d9d49-129">A provider added by **AddPrintProvidor** may be removed by calling [**DeletePrintProvidor**](deleteprintprovidor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d49-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9d49-130">Requirements</span></span>



| <span data-ttu-id="d9d49-131">需求</span><span class="sxs-lookup"><span data-stu-id="d9d49-131">Requirement</span></span> | <span data-ttu-id="d9d49-132">值</span><span class="sxs-lookup"><span data-stu-id="d9d49-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d49-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9d49-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d49-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9d49-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d9d49-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9d49-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d49-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9d49-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d9d49-137">標頭</span><span class="sxs-lookup"><span data-stu-id="d9d49-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9d49-138"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d9d49-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d9d49-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="d9d49-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9d49-140"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9d49-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d9d49-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d9d49-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9d49-142"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="d9d49-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d9d49-143">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d9d49-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d9d49-144">**AddPrintProvidorW** (Unicode) 和 **AddPrintProvidorA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d9d49-144">**AddPrintProvidorW** (Unicode) and **AddPrintProvidorA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="d9d49-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9d49-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d49-146">列印</span><span class="sxs-lookup"><span data-stu-id="d9d49-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d9d49-147">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="d9d49-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d9d49-148">**DeletePrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="d9d49-148">**DeletePrintProvidor**</span></span>](deleteprintprovidor.md)
</dt> <dt>

[<span data-ttu-id="d9d49-149">**PROVIDOR \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d9d49-149">**PROVIDOR\_INFO\_1**</span></span>](providor-info-1.md)
</dt> <dt>

[<span data-ttu-id="d9d49-150">**PROVIDOR \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d9d49-150">**PROVIDOR\_INFO\_2**</span></span>](providor-info-2.md)
</dt> </dl>

 

 




