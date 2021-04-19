---
description: GetPrinter 函式會捕獲指定印表機的相關資訊。
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: 'GetPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985098"
---
# <a name="getprinter-function"></a><span data-ttu-id="d5f66-103">GetPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="d5f66-103">GetPrinter function</span></span>

<span data-ttu-id="d5f66-104">**GetPrinter** 函式會捕獲指定印表機的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5f66-104">The **GetPrinter** function retrieves information about a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f66-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5f66-105">Syntax</span></span>


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="d5f66-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5f66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f66-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5f66-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f66-108">函式用來抓取資訊之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d5f66-108">A handle to the printer for which the function retrieves information.</span></span> <span data-ttu-id="d5f66-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="d5f66-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d5f66-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5f66-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f66-111">函數儲存在 *pPrinter* 所指向之緩衝區中的結構層級或類型。</span><span class="sxs-lookup"><span data-stu-id="d5f66-111">The level or type of structure that the function stores into the buffer pointed to by *pPrinter*.</span></span>

<span data-ttu-id="d5f66-112">此值可以是1、2、3、4、5、6、7、8或9。</span><span class="sxs-lookup"><span data-stu-id="d5f66-112">This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.</span></span>

</dd> <dt>

<span data-ttu-id="d5f66-113">*pPrinter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d5f66-113">*pPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f66-114">緩衝區的指標，此緩衝區會接收包含指定印表機相關資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="d5f66-114">A pointer to a buffer that receives a structure containing information about the specified printer.</span></span> <span data-ttu-id="d5f66-115">緩衝區必須夠大，才能接收結構以及結構成員指向的任何字串或其他資料。</span><span class="sxs-lookup"><span data-stu-id="d5f66-115">The buffer must be large enough to receive the structure and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="d5f66-116">如果緩衝區太小， *pcbNeeded* 參數會傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d5f66-116">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

<span data-ttu-id="d5f66-117">結構的類型取決於 *層級* 的值。</span><span class="sxs-lookup"><span data-stu-id="d5f66-117">The type of structure is determined by the value of *Level*.</span></span>



| <span data-ttu-id="d5f66-118">層級</span><span class="sxs-lookup"><span data-stu-id="d5f66-118">Level</span></span>                                                                                                | <span data-ttu-id="d5f66-119">結構</span><span class="sxs-lookup"><span data-stu-id="d5f66-119">Structure</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d5f66-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-120"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d5f66-121">包含一般印表機資訊的 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d5f66-121">A [**PRINTER\_INFO\_1**](printer-info-1.md) structure containing general printer information.</span></span><br/>                                                                                                        |
| <span id="2"></span><dl> <span data-ttu-id="d5f66-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-122"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d5f66-123">[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構，內含印表機的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d5f66-123">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                             |
| <span id="3"></span><dl> <span data-ttu-id="d5f66-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d5f66-125">[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)結構，內含印表機的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="d5f66-125">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                 |
| <span id="4"></span><dl> <span data-ttu-id="d5f66-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d5f66-127">[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)結構，其中包含最少量的印表機資訊，包括印表機的名稱、伺服器的名稱，以及印表機是否為遠端或本機。</span><span class="sxs-lookup"><span data-stu-id="d5f66-127">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="d5f66-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-128"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="d5f66-129">[**印表機 \_ 資訊 \_ 5**](printer-info-5.md)結構，包含印表機屬性和超時設定等印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="d5f66-129">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                               |
| <span id="6"></span><dl> <span data-ttu-id="d5f66-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-130"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="d5f66-131">[**印表機 \_ 資訊 \_ 6**](printer-info-6.md)結構，指定印表機的狀態值。</span><span class="sxs-lookup"><span data-stu-id="d5f66-131">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                      |
| <span id="7"></span><dl> <span data-ttu-id="d5f66-132"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-132"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="d5f66-133">[**印表機 \_ 資訊 \_ 7**](printer-info-7.md)結構，指出是否在目錄服務中發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="d5f66-133">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure that indicates whether the printer is published in the directory service.</span></span><br/>                                                                      |
| <span id="8"></span><dl> <span data-ttu-id="d5f66-134"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-134"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="d5f66-135">[**印表機 \_ 資訊 \_ 8**](printer-info-8.md)結構，指定全域預設印表機設定。</span><span class="sxs-lookup"><span data-stu-id="d5f66-135">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                |
| <span id="9"></span><dl> <span data-ttu-id="d5f66-136"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-136"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="d5f66-137">[**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構，指定每個使用者的預設印表機設定。</span><span class="sxs-lookup"><span data-stu-id="d5f66-137">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="d5f66-138">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5f66-138">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f66-139">*PPrinter* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5f66-139">The size, in bytes, of the buffer pointed to by *pPrinter*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f66-140">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d5f66-140">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f66-141">變數的指標，此函式會將其設定為印表機資訊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5f66-141">A pointer to a variable that the function sets to the size, in bytes, of the printer information.</span></span> <span data-ttu-id="d5f66-142">如果 *cbBuf* 小於此值，則 **GetPrinter** 會失敗，而值代表所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d5f66-142">If *cbBuf* is smaller than this value, **GetPrinter** fails, and the value represents the required buffer size.</span></span> <span data-ttu-id="d5f66-143">如果 *cbBuf* 等於或大於此值， **GetPrinter** 會成功，而值代表緩衝區中儲存的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d5f66-143">If *cbBuf* is equal to or greater than this value, **GetPrinter** succeeds, and the value represents the number of bytes stored in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f66-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5f66-144">Return value</span></span>

<span data-ttu-id="d5f66-145">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="d5f66-145">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d5f66-146">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="d5f66-146">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f66-147">備註</span><span class="sxs-lookup"><span data-stu-id="d5f66-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5f66-148">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="d5f66-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d5f66-149">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="d5f66-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d5f66-150">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="d5f66-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d5f66-151">[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)、[**印表機 \_ 資訊 \_ 8**](printer-info-8.md)和 [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構中的 **pDevMode** 成員可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d5f66-151">The **pDevMode** member in the [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_8**](printer-info-8.md), and [**PRINTER\_INFO\_9**](printer-info-9.md) structures can be **NULL**.</span></span> <span data-ttu-id="d5f66-152">發生這種情況時，印表機會無法使用，直到重新安裝驅動程式為止。</span><span class="sxs-lookup"><span data-stu-id="d5f66-152">When this happens, the printer is unusable until the driver is reinstalled successfully.</span></span>

<span data-ttu-id="d5f66-153">針對包含安全描述項指標的 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 和 [**印表機 \_ 資訊 \_ 3**](printer-info-3.md) 結構，此函式只會抓取呼叫端有權讀取之安全描述項的元件。</span><span class="sxs-lookup"><span data-stu-id="d5f66-153">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read.</span></span> <span data-ttu-id="d5f66-154">若要取得特定的安全描述項元件，您必須在呼叫 [**OpenPrinter**](openprinter.md) 函式來取得印表機的控制碼時，指定必要的存取權限。</span><span class="sxs-lookup"><span data-stu-id="d5f66-154">To retrieve particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="d5f66-155">下表顯示讀取各種安全描述項元件所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="d5f66-155">The following table shows the access rights required to read the various security descriptor components.</span></span>



| <span data-ttu-id="d5f66-156">存取權限</span><span class="sxs-lookup"><span data-stu-id="d5f66-156">Access Right</span></span>                        | <span data-ttu-id="d5f66-157">安全描述項元件</span><span class="sxs-lookup"><span data-stu-id="d5f66-157">Security Descriptor Component</span></span>                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f66-158">讀取 \_ 控制</span><span class="sxs-lookup"><span data-stu-id="d5f66-158">READ\_CONTROL</span></span><br/>            | <span data-ttu-id="d5f66-159">擁有者</span><span class="sxs-lookup"><span data-stu-id="d5f66-159">Owner</span></span><br/> <span data-ttu-id="d5f66-160">主要群組</span><span class="sxs-lookup"><span data-stu-id="d5f66-160">Primary group</span></span><br/> <span data-ttu-id="d5f66-161">任意存取控制清單 (DACL) </span><span class="sxs-lookup"><span data-stu-id="d5f66-161">Discretionary access-control list (DACL)</span></span><br/> |
| <span data-ttu-id="d5f66-162">存取 \_ 系統 \_ 安全性</span><span class="sxs-lookup"><span data-stu-id="d5f66-162">ACCESS\_SYSTEM\_SECURITY</span></span><br/> | <span data-ttu-id="d5f66-163">系統存取控制清單 (SACL) </span><span class="sxs-lookup"><span data-stu-id="d5f66-163">System access-control list (SACL)</span></span><br/>                                                  |



 

<span data-ttu-id="d5f66-164">如果您指定層級7，則 [**印表機 \_ 資訊 \_ 7**](printer-info-7.md)的 **dwAction** 成員會傳回下列其中一個值，指出是否在目錄服務中發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="d5f66-164">If you specify level 7, the **dwAction** member of [**PRINTER\_INFO\_7**](printer-info-7.md) returns one of the following values to indicate whether the printer is published in the directory service.</span></span>



| <span data-ttu-id="d5f66-165">dwAction 值</span><span class="sxs-lookup"><span data-stu-id="d5f66-165">dwAction value</span></span>     | <span data-ttu-id="d5f66-166">意義</span><span class="sxs-lookup"><span data-stu-id="d5f66-166">Meaning</span></span>                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f66-167">DSPRINT \_ 發行</span><span class="sxs-lookup"><span data-stu-id="d5f66-167">DSPRINT\_PUBLISH</span></span>   | <span data-ttu-id="d5f66-168">印表機已發佈。</span><span class="sxs-lookup"><span data-stu-id="d5f66-168">The printer is published.</span></span> <span data-ttu-id="d5f66-169">**PszObjectGUID** 成員包含與印表機相關聯之目錄服務列印佇列物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d5f66-169">The **pszObjectGUID** member contains the GUID of the directory services print queue object associated with the printer.</span></span>                                                                                                       |
| <span data-ttu-id="d5f66-170">DSPRINT \_ 取消發佈</span><span class="sxs-lookup"><span data-stu-id="d5f66-170">DSPRINT\_UNPUBLISH</span></span> | <span data-ttu-id="d5f66-171">未發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="d5f66-171">The printer is not published.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="d5f66-172">DSPRINT \_ 暫止</span><span class="sxs-lookup"><span data-stu-id="d5f66-172">DSPRINT\_PENDING</span></span>   | <span data-ttu-id="d5f66-173">指出系統正在嘗試完成發行或取消發行作業。</span><span class="sxs-lookup"><span data-stu-id="d5f66-173">Indicates that the system is attempting to complete a publish or unpublish operation.</span></span> <span data-ttu-id="d5f66-174">如果 [**SetPrinter**](setprinter.md) 呼叫無法發行或取消發行印表機，系統會進一步嘗試在背景中完成此作業。</span><span class="sxs-lookup"><span data-stu-id="d5f66-174">If a [**SetPrinter**](setprinter.md) call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</span></span> |



 

<span data-ttu-id="d5f66-175">從 Windows Vista 開始，當 *hPrinter* 參考列印伺服器所裝載的印表機，而且至少有一個開啟的列印伺服器連線時，就會從本機快取中取出 **GetPrinter** 傳回的印表機資料。</span><span class="sxs-lookup"><span data-stu-id="d5f66-175">Starting with Windows Vista, the printer data returned by **GetPrinter** is retrieved from a local cache when *hPrinter* refers to a printer hosted by a print server and there is at least one open connection to the print server.</span></span> <span data-ttu-id="d5f66-176">在所有其他設定中，會從列印伺服器查詢印表機資料。</span><span class="sxs-lookup"><span data-stu-id="d5f66-176">In all other configurations, the printer data is queried from the print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f66-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5f66-177">Requirements</span></span>



| <span data-ttu-id="d5f66-178">需求</span><span class="sxs-lookup"><span data-stu-id="d5f66-178">Requirement</span></span> | <span data-ttu-id="d5f66-179">值</span><span class="sxs-lookup"><span data-stu-id="d5f66-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f66-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5f66-180">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f66-181">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5f66-181">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d5f66-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5f66-182">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f66-183">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5f66-183">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d5f66-184">標頭</span><span class="sxs-lookup"><span data-stu-id="d5f66-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f66-185"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-185"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d5f66-186">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5f66-186">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5f66-187"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-187"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d5f66-188">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f66-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f66-189"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="d5f66-189"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d5f66-190">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d5f66-190">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5f66-191">**GetPrinterW** (Unicode) 和 **GetPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d5f66-191">**GetPrinterW** (Unicode) and **GetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="d5f66-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5f66-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f66-193">列印</span><span class="sxs-lookup"><span data-stu-id="d5f66-193">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d5f66-194">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="d5f66-194">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d5f66-195">**AbortPrinter**</span><span class="sxs-lookup"><span data-stu-id="d5f66-195">**AbortPrinter**</span></span>](abortprinter.md)
</dt> <dt>

[<span data-ttu-id="d5f66-196">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="d5f66-196">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="d5f66-197">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="d5f66-197">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="d5f66-198">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="d5f66-198">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="d5f66-199">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="d5f66-199">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="d5f66-200">**印表機 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d5f66-200">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="d5f66-201">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d5f66-201">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="d5f66-202">**印表機 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="d5f66-202">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="d5f66-203">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="d5f66-203">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="d5f66-204">**印表機 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="d5f66-204">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="d5f66-205">**印表機 \_ 資訊 \_ 7**</span><span class="sxs-lookup"><span data-stu-id="d5f66-205">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="d5f66-206">**印表機 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="d5f66-206">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="d5f66-207">**印表機 \_ 資訊 \_ 9**</span><span class="sxs-lookup"><span data-stu-id="d5f66-207">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="d5f66-208">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d5f66-208">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d5f66-209">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="d5f66-209">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




