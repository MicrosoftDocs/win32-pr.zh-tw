---
description: DeletePrinterDriver 函數會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱。
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: 'DeletePrinterDriver 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974435"
---
# <a name="deleteprinterdriver-function"></a><span data-ttu-id="e230f-103">DeletePrinterDriver 函式</span><span class="sxs-lookup"><span data-stu-id="e230f-103">DeletePrinterDriver function</span></span>

<span data-ttu-id="e230f-104">**DeletePrinterDriver** 函數會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e230f-104">The **DeletePrinterDriver** function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span>

<span data-ttu-id="e230f-105">若要刪除與驅動程式相關聯的檔案，以及從伺服器支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，請使用 [**DeletePrinterDriverEx**](deleteprinterdriverex.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="e230f-105">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the [**DeletePrinterDriverEx**](deleteprinterdriverex.md) function.</span></span>

<span data-ttu-id="e230f-106">只有當指定的環境未使用任何驅動程式版本時， **DeletePrinterDriver** 才會刪除驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e230f-106">**DeletePrinterDriver** deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="e230f-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) 可以刪除特定版本的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e230f-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) can delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="e230f-108">語法</span><span class="sxs-lookup"><span data-stu-id="e230f-108">Syntax</span></span>


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a><span data-ttu-id="e230f-109">參數</span><span class="sxs-lookup"><span data-stu-id="e230f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e230f-110">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e230f-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e230f-111">以 null 結束的字串指標，指定要從中刪除驅動程式之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e230f-111">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="e230f-112">如果此參數為 **Null**，則會在本機移除印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e230f-112">If this parameter is **NULL**, the printer-driver name will be removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="e230f-113">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e230f-113">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e230f-114">以 null 結束的字串指標，指定要從中刪除驅動程式 (例如，Windows x86、Windows IA64 或 Windows x64) 的環境。</span><span class="sxs-lookup"><span data-stu-id="e230f-114">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="e230f-115">如果此參數為 **Null**，則會從目前的呼叫應用程式和用戶端電腦的環境中刪除驅動程式名稱， (不是目的地應用程式和列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="e230f-115">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="e230f-116">*pDriverName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e230f-116">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e230f-117">以 null 結束的字串指標，指定應該刪除之驅動程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e230f-117">A pointer to a null-terminated string specifying the name of the driver that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e230f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e230f-118">Return value</span></span>

<span data-ttu-id="e230f-119">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="e230f-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e230f-120">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e230f-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e230f-121">備註</span><span class="sxs-lookup"><span data-stu-id="e230f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e230f-122">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e230f-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e230f-123">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e230f-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e230f-124">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e230f-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e230f-125">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="e230f-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="e230f-126">**DeletePrinterDriver** 函式不會刪除相關聯的檔案，只會從 [**EnumPrinterDrivers**](enumprinterdrivers.md)函數所傳回的清單中移除驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e230f-126">The **DeletePrinterDriver** function does not delete the associated files, it merely removes the driver name from the list returned by the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="e230f-127">在呼叫 **DeletePrinterDriver** 之前，您必須刪除所有使用印表機驅動程式的印表機物件。</span><span class="sxs-lookup"><span data-stu-id="e230f-127">Before calling **DeletePrinterDriver**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="e230f-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e230f-128">Requirements</span></span>



| <span data-ttu-id="e230f-129">需求</span><span class="sxs-lookup"><span data-stu-id="e230f-129">Requirement</span></span> | <span data-ttu-id="e230f-130">值</span><span class="sxs-lookup"><span data-stu-id="e230f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e230f-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e230f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e230f-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e230f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e230f-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e230f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e230f-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e230f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e230f-135">標頭</span><span class="sxs-lookup"><span data-stu-id="e230f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e230f-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e230f-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e230f-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="e230f-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e230f-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e230f-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e230f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e230f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e230f-140"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="e230f-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e230f-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e230f-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e230f-142">**DeletePrinterDriverW** (Unicode) 和 **DeletePrinterDriverA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e230f-142">**DeletePrinterDriverW** (Unicode) and **DeletePrinterDriverA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e230f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e230f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e230f-144">列印</span><span class="sxs-lookup"><span data-stu-id="e230f-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e230f-145">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e230f-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e230f-146">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="e230f-146">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="e230f-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="e230f-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

