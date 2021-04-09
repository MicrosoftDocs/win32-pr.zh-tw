---
description: '>enumprinters 函式會列舉可用的印表機、列印伺服器、網域或列印提供者。'
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: '>enumprinters 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849217"
---
# <a name="enumprinters-function"></a><span data-ttu-id="aed33-103">>enumprinters 函式</span><span class="sxs-lookup"><span data-stu-id="aed33-103">EnumPrinters function</span></span>

<span data-ttu-id="aed33-104">**>enumprinters** 函式會列舉可用的印表機、列印伺服器、網域或列印提供者。</span><span class="sxs-lookup"><span data-stu-id="aed33-104">The **EnumPrinters** function enumerates available printers, print servers, domains, or print providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed33-105">語法</span><span class="sxs-lookup"><span data-stu-id="aed33-105">Syntax</span></span>


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="aed33-106">參數</span><span class="sxs-lookup"><span data-stu-id="aed33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aed33-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="aed33-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed33-108">函數應該列舉的列印物件類型。</span><span class="sxs-lookup"><span data-stu-id="aed33-108">The types of print objects that the function should enumerate.</span></span> <span data-ttu-id="aed33-109">這個值可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="aed33-109">This value can be one or more of the following values.</span></span>



| <span data-ttu-id="aed33-110">值</span><span class="sxs-lookup"><span data-stu-id="aed33-110">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="aed33-111">意義</span><span class="sxs-lookup"><span data-stu-id="aed33-111">Meaning</span></span>                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <span data-ttu-id="aed33-112"><dt>**印表機 \_ 列舉 \_ 區域**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-112"><dt>**PRINTER\_ENUM\_LOCAL**</dt></span></span> </dl>                       | <span data-ttu-id="aed33-113">如果 \_ \_ 未同時傳遞印表機列舉名稱旗標，此函式會忽略 *NAME* 參數，並列舉本機安裝的印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-113">If the PRINTER\_ENUM\_NAME flag is not also passed, the function ignores the *Name* parameter, and enumerates the locally installed printers.</span></span> <span data-ttu-id="aed33-114">如果 \_ \_ 也傳遞印表機列舉名稱，此函式會列舉本機印表機的 *名稱*。</span><span class="sxs-lookup"><span data-stu-id="aed33-114">If PRINTER\_ENUM\_NAME is also passed, the function enumerates the local printers on *Name*.</span></span> <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <span data-ttu-id="aed33-115"><dt>**印表機 \_ 列舉 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-115"><dt>**PRINTER\_ENUM\_NAME**</dt></span></span> </dl>                          | <span data-ttu-id="aed33-116">函數會列舉依 *名稱* 識別的印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-116">The function enumerates the printer identified by *Name*.</span></span> <span data-ttu-id="aed33-117">這可以是伺服器、網域或列印提供者。</span><span class="sxs-lookup"><span data-stu-id="aed33-117">This can be a server, a domain, or a print provider.</span></span> <span data-ttu-id="aed33-118">如果 *Name* 為 **Null**，則函式會列舉可用的列印提供者。</span><span class="sxs-lookup"><span data-stu-id="aed33-118">If *Name* is **NULL**, the function enumerates available print providers.</span></span><br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <span data-ttu-id="aed33-119"><dt>**印表機 \_ 列舉 \_ 共用**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-119"><dt>**PRINTER\_ENUM\_SHARED**</dt></span></span> </dl>                    | <span data-ttu-id="aed33-120">此函數會列舉具有共用屬性的印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-120">The function enumerates printers that have the shared attribute.</span></span> <span data-ttu-id="aed33-121">無法在隔離中使用;使用或作業來結合另一個印表機 \_ 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="aed33-121">Cannot be used in isolation; use an OR operation to combine with another PRINTER\_ENUM type.</span></span><br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <span data-ttu-id="aed33-122"><dt>**印表機 \_ 列舉 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-122"><dt>**PRINTER\_ENUM\_CONNECTIONS**</dt></span></span> </dl>     | <span data-ttu-id="aed33-123">此函式會列舉使用者對其進行先前連接的印表機清單。</span><span class="sxs-lookup"><span data-stu-id="aed33-123">The function enumerates the list of printers to which the user has made previous connections.</span></span><br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <span data-ttu-id="aed33-124"><dt>**印表機 \_ 列舉 \_ 網路**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-124"><dt>**PRINTER\_ENUM\_NETWORK**</dt></span></span> </dl>                 | <span data-ttu-id="aed33-125">此函數會列舉電腦網域中的網路印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-125">The function enumerates network printers in the computer's domain.</span></span> <span data-ttu-id="aed33-126">只有當 *層級* 為1時，此值才有效。</span><span class="sxs-lookup"><span data-stu-id="aed33-126">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <span data-ttu-id="aed33-127"><dt>**印表機 \_ 列舉 \_ 遠端**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-127"><dt>**PRINTER\_ENUM\_REMOTE**</dt></span></span> </dl>                    | <span data-ttu-id="aed33-128">此函數會列舉電腦網域中的網路印表機和列印伺服器。</span><span class="sxs-lookup"><span data-stu-id="aed33-128">The function enumerates network printers and print servers in the computer's domain.</span></span> <span data-ttu-id="aed33-129">只有當 *層級* 為1時，此值才有效。</span><span class="sxs-lookup"><span data-stu-id="aed33-129">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <span data-ttu-id="aed33-130"><dt>**印表機 \_ 列舉 \_ 類別 \_ 3d**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-130"><dt>**PRINTER\_ENUM\_CATEGORY\_3D**</dt></span></span> </dl>    | <span data-ttu-id="aed33-131">此函數只會列舉3D 印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-131">The function enumerates only 3D printers.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <span data-ttu-id="aed33-132"><dt>**印表機 \_ 列舉 \_ 類別目錄 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-132"><dt>**PRINTER\_ENUM\_CATEGORY\_ALL**</dt></span></span> </dl> | <span data-ttu-id="aed33-133">此函數會列舉所有列印裝置，包括3D 印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-133">The function enumerates all print devices, including 3D printers.</span></span><br/>                                                                                                                                                                           |



 

<span data-ttu-id="aed33-134">如果 *層級* 為4，您只能使用印表機 \_ 列舉 \_ 連接和印表機 \_ 列舉 \_ 本機常數。</span><span class="sxs-lookup"><span data-stu-id="aed33-134">If *Level* is 4, you can only use the PRINTER\_ENUM\_CONNECTIONS and PRINTER\_ENUM\_LOCAL constants.</span></span>

> [!Note]  
> <span data-ttu-id="aed33-135">預設不會列舉3D 列印裝置。</span><span class="sxs-lookup"><span data-stu-id="aed33-135">3D print devices are not enumerated by default.</span></span> <span data-ttu-id="aed33-136">您必須同時包含 **印表機 \_ 列舉 \_ 類別 \_ 3d** 和 **印表機 \_ 列舉 \_ 區域** ，才能列舉3d 印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-136">You must include both **PRINTER\_ENUM\_CATEGORY\_3D** and **PRINTER\_ENUM\_LOCAL** to enumerate only 3D printers.</span></span> <span data-ttu-id="aed33-137">若要包含3D 印表機以及所有其他本機印表機，請使用 [ **印表機 \_ 列舉 \_ 類別 \_** ] 和 [ **印表機 \_ 列舉 \_ 本機**]。</span><span class="sxs-lookup"><span data-stu-id="aed33-137">To include 3D printers, along with all other local printers, use **PRINTER\_ENUM\_CATEGORY\_ALL** and **PRINTER\_ENUM\_LOCAL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="aed33-138">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aed33-138">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed33-139">如果 *層級* 為1， *旗標* 就會包含印表機 \_ 列舉 \_ 名稱，而 *名稱* 為非 **null**，則 *name* 是以 null 結束的字串指標，可指定要列舉的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="aed33-139">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is non-**NULL**, then *Name* is a pointer to a null-terminated string that specifies the name of the object to enumerate.</span></span> <span data-ttu-id="aed33-140">這個字串可以是伺服器、網域或列印提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="aed33-140">This string can be the name of a server, a domain, or a print provider.</span></span>

<span data-ttu-id="aed33-141">如果 *層級* 為1， *旗標* 就會包含印表機 \_ 列舉 \_ 名稱，而 *名稱* 是 **Null**，則函式會列舉可用的列印提供者。</span><span class="sxs-lookup"><span data-stu-id="aed33-141">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is **NULL**, then the function enumerates the available print providers.</span></span>

<span data-ttu-id="aed33-142">如果 *層級* 為1， *旗標* 就會包含印表機 \_ ENUM \_ REMOTE，而 *Name* 是 **Null**，則函式會列舉使用者網域中的印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-142">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_REMOTE, and *Name* is **NULL**, then the function enumerates the printers in the user's domain.</span></span>

<span data-ttu-id="aed33-143">如果 *層級* 為2或5，則 *名稱* 是以 null 結束的字串指標，可指定要列舉其印表機的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="aed33-143">If *Level* is 2 or 5,*Name* is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated.</span></span> <span data-ttu-id="aed33-144">如果此字串為 **Null**，則此函式會列舉本機電腦上安裝的印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-144">If this string is **NULL**, then the function enumerates the printers installed on the local computer.</span></span>

<span data-ttu-id="aed33-145">如果 *層級* 為4，則 *名稱* 應該是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aed33-145">If *Level* is 4, *Name* should be **NULL**.</span></span> <span data-ttu-id="aed33-146">函數一律會在本機電腦上進行查詢。</span><span class="sxs-lookup"><span data-stu-id="aed33-146">The function always queries on the local computer.</span></span>

<span data-ttu-id="aed33-147">當 *名稱* 為 **Null** 時，將 *旗標* 設定為印表機 \_ 列舉 \_ 本機 \| 印表機 \_ 列舉 \_ 連接會列舉安裝在本機電腦上的印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-147">When *Name* is **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_CONNECTIONS enumerates printers that are installed on the local machine.</span></span> <span data-ttu-id="aed33-148">這些印表機包括實際連接到本機電腦的印表機，以及具有網路連線的遠端印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-148">These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.</span></span>

<span data-ttu-id="aed33-149">當 *Name* 不是 **Null** 時，將 *旗標* 設定為印表機 \_ 列舉 \_ 本機 \| 印表機 \_ 列舉 \_ 名稱會列舉安裝在伺服器 *名稱* 上的本機印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-149">When *Name* is not **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_NAME enumerates the local printers that are installed on the server *Name*.</span></span>

</dd> <dt>

<span data-ttu-id="aed33-150">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aed33-150">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed33-151">*PPrinterEnum* 所指向的資料結構類型。</span><span class="sxs-lookup"><span data-stu-id="aed33-151">The type of data structures pointed to by *pPrinterEnum*.</span></span> <span data-ttu-id="aed33-152">有效的值為1、2、4和5，其對應于 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md)、 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 、 [**印表機 \_ 資訊 \_ 4**](printer-info-4.md)和 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="aed33-152">Valid values are 1, 2, 4, and 5, which correspond to the [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), and [**PRINTER\_INFO\_5**](printer-info-5.md) data structures.</span></span>

<span data-ttu-id="aed33-153">此值可以是1、2、4或5。</span><span class="sxs-lookup"><span data-stu-id="aed33-153">This value can be 1, 2, 4, or 5.</span></span>

</dd> <dt>

<span data-ttu-id="aed33-154">*pPrinterEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aed33-154">*pPrinterEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aed33-155">緩衝區的指標，此緩衝區會接收 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md)、 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)、 [**印表機 \_ 資訊 \_ 4**](printer-info-4.md)或 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="aed33-155">A pointer to a buffer that receives an array of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span> <span data-ttu-id="aed33-156">每個結構都包含描述可用列印物件的資料。</span><span class="sxs-lookup"><span data-stu-id="aed33-156">Each structure contains data that describes an available print object.</span></span>

<span data-ttu-id="aed33-157">如果 *層級* 為1，則陣列包含 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="aed33-157">If *Level* is 1, the array contains [**PRINTER\_INFO\_1**](printer-info-1.md) structures.</span></span> <span data-ttu-id="aed33-158">如果 *層級* 為2，則陣列會包含 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="aed33-158">If *Level* is 2, the array contains [**PRINTER\_INFO\_2**](printer-info-2.md) structures.</span></span> <span data-ttu-id="aed33-159">如果 *層級* 為4，則陣列包含 [**印表機 \_ 資訊 \_ 4**](printer-info-4.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="aed33-159">If *Level* is 4, the array contains [**PRINTER\_INFO\_4**](printer-info-4.md) structures.</span></span> <span data-ttu-id="aed33-160">如果 *層級* 為5，則陣列包含 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="aed33-160">If *Level* is 5, the array contains [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span>

<span data-ttu-id="aed33-161">緩衝區必須夠大，才能接收資料結構的陣列，以及結構成員指向的任何字串或其他資料。</span><span class="sxs-lookup"><span data-stu-id="aed33-161">The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="aed33-162">如果緩衝區太小， *pcbNeeded* 參數會傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="aed33-162">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="aed33-163">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aed33-163">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed33-164">*PPrinterEnum* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aed33-164">The size, in bytes, of the buffer pointed to by *pPrinterEnum*.</span></span>

</dd> <dt>

<span data-ttu-id="aed33-165">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aed33-165">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aed33-166">值的指標，如果函式成功則為，如果 *cbBuf* 太小，則會收到所需的位元組數目，以接收復制的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="aed33-166">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="aed33-167">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aed33-167">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aed33-168">值的指標，此值會接收在 *pPrinterEnum* 點的陣列中，此函式所傳回的 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md)、[**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 、[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)或 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md)結構的數目。</span><span class="sxs-lookup"><span data-stu-id="aed33-168">A pointer to a value that receives the number of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures that the function returns in the array to which *pPrinterEnum* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aed33-169">傳回值</span><span class="sxs-lookup"><span data-stu-id="aed33-169">Return value</span></span>

<span data-ttu-id="aed33-170">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="aed33-170">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="aed33-171">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="aed33-171">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aed33-172">備註</span><span class="sxs-lookup"><span data-stu-id="aed33-172">Remarks</span></span>

<span data-ttu-id="aed33-173">請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="aed33-173">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="aed33-174">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="aed33-174">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="aed33-175">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="aed33-175">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="aed33-176">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="aed33-176">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="aed33-177">如果 **>enumprinters** 傳回印表機列舉容器所指定的 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md) 結構 \_ \_ ，則表示有印表機物件的階層。</span><span class="sxs-lookup"><span data-stu-id="aed33-177">If **EnumPrinters** returns a [**PRINTER\_INFO\_1**](printer-info-1.md) structure in which PRINTER\_ENUM\_CONTAINER is specified, this indicates that there is a hierarchy of printer objects.</span></span> <span data-ttu-id="aed33-178">應用程式可以再次呼叫 **>enumprinters** 來列舉階層，並將 *名稱* 設定為 **印表機 \_ 資訊 \_ 1** 結構的 **pName** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="aed33-178">An application can enumerate the hierarchy by calling **EnumPrinters** again, setting *Name* to the value of the **PRINTER\_INFO\_1** structure's **pName** member.</span></span>

<span data-ttu-id="aed33-179">**>enumprinters** 函數不會取得安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="aed33-179">The **EnumPrinters** function does not retrieve security information.</span></span> <span data-ttu-id="aed33-180">如果 *pPrinterEnum* 所指向的陣列中傳回 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構，其 *pSecurityDescriptor* 成員將會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aed33-180">If [**PRINTER\_INFO\_2**](printer-info-2.md) structures are returned in the array pointed to by *pPrinterEnum*, their *pSecurityDescriptor* members will be set to **NULL**.</span></span>

<span data-ttu-id="aed33-181">若要取得預設印表機的相關資訊，請呼叫 [**GetDefaultPrinter**](getdefaultprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="aed33-181">To get information about the default printer, call [**GetDefaultPrinter**](getdefaultprinter.md).</span></span>

<span data-ttu-id="aed33-182">[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)結構提供簡單且極快速的方式來抓取本機電腦上安裝的印表機名稱，以及使用者已建立的遠端連線。</span><span class="sxs-lookup"><span data-stu-id="aed33-182">The [**PRINTER\_INFO\_4**](printer-info-4.md) structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="aed33-183">使用 **印表機 \_ 資訊 \_ 4** 資料結構呼叫 **>enumprinters** 時，該函式會查詢登錄中的指定資訊，然後立即傳回。</span><span class="sxs-lookup"><span data-stu-id="aed33-183">When **EnumPrinters** is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="aed33-184">這與其他層級的 **印表機 \_ 資訊 \_ \* *_ 資料結構一起呼叫時，與 >enumprinters 的行為不同。尤其是當*** 使用層級 2 ([**印表機 \_ 資訊 \_ 2**](printer-info-2.md)) 資料結構來呼叫 _ >enumprinters 時，它會在每個遠端連線上執行 [**OpenPrinter**](openprinter.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="aed33-184">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_\**_ data structures. In particular, when _\* EnumPrinters*\* is called with a level 2 ([**PRINTER\_INFO\_2**](printer-info-2.md)) data structure, it performs an [**OpenPrinter**](openprinter.md) call on each remote connection.</span></span> <span data-ttu-id="aed33-185">如果遠端連線已關閉，或遠端伺服器已不存在，或遠端印表機已不存在，則函式必須等待 RPC 超時，進而使 **OpenPrinter** 呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="aed33-185">If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="aed33-186">這可能需要一段時間。</span><span class="sxs-lookup"><span data-stu-id="aed33-186">This can take a while.</span></span> <span data-ttu-id="aed33-187">傳遞 **印表機 \_ 資訊 \_ 4** 結構，可讓應用程式取出最少的必要資訊; 如果需要更詳細的資訊，則可以進行後續的 **>enumprinters** 層級2呼叫。</span><span class="sxs-lookup"><span data-stu-id="aed33-187">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinters** level 2 call can be made.</span></span>

<span data-ttu-id="aed33-188">**Windows Vista：** 當 *層級* 的值為4時，會從本機快取中取出 **>enumprinters** 傳回的印表機資料。</span><span class="sxs-lookup"><span data-stu-id="aed33-188">**Windows Vista:** The printer data returned by **EnumPrinters** is retrieved from a local cache when the value of *Level* is 4.</span></span>

<span data-ttu-id="aed33-189">下表顯示當 *Level* 參數設定為1時，各種 *旗標* 值的 **>enumprinters** 輸出。</span><span class="sxs-lookup"><span data-stu-id="aed33-189">The following table shows the **EnumPrinters** output for various *Flags* values when the *Level* parameter is set to 1.</span></span>

<span data-ttu-id="aed33-190">在資料表的 [ *名稱* 參數] 欄中，您應該以適當的名稱取代列印提供者、網域和電腦。</span><span class="sxs-lookup"><span data-stu-id="aed33-190">In the *Name* parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine.</span></span> <span data-ttu-id="aed33-191">例如，針對「列印提供者」，您可以使用網路列印提供者的名稱或本機列印提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="aed33-191">For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider.</span></span> <span data-ttu-id="aed33-192">若要取出列印提供者名稱，請呼叫 *名稱* 設為 **Null** 的 **>enumprinters** 。</span><span class="sxs-lookup"><span data-stu-id="aed33-192">To retrieve print provider names, call **EnumPrinters** with *Name* set to **NULL**.</span></span>



| <span data-ttu-id="aed33-193">*旗標* 參數</span><span class="sxs-lookup"><span data-stu-id="aed33-193">*Flags* parameter</span></span>                                  | <span data-ttu-id="aed33-194">*Name* 參數</span><span class="sxs-lookup"><span data-stu-id="aed33-194">*Name* parameter</span></span>                            | <span data-ttu-id="aed33-195">結果</span><span class="sxs-lookup"><span data-stu-id="aed33-195">Result</span></span>                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aed33-196">印表機 \_ 列舉 \_ 本機 (而非印表機 \_ 列舉 \_ 名稱) </span><span class="sxs-lookup"><span data-stu-id="aed33-196">PRINTER\_ENUM\_LOCAL (and not PRINTER\_ENUM\_NAME)</span></span> | <span data-ttu-id="aed33-197">*Name* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="aed33-197">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="aed33-198">所有本機印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-198">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="aed33-199">印表機 \_ 列舉 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="aed33-199">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="aed33-200">「列印提供者」</span><span class="sxs-lookup"><span data-stu-id="aed33-200">"Print Provider"</span></span><br/>                 | <span data-ttu-id="aed33-201">所有功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="aed33-201">All domain names</span></span><br/>                                                                       |
| <span data-ttu-id="aed33-202">印表機 \_ 列舉 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="aed33-202">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="aed33-203">「列印提供者！局域</span><span class="sxs-lookup"><span data-stu-id="aed33-203">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="aed33-204">電腦網域中的所有印表機和列印伺服器</span><span class="sxs-lookup"><span data-stu-id="aed33-204">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="aed33-205">印表機 \_ 列舉 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="aed33-205">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="aed33-206">「列印提供者！ \\ \\設備</span><span class="sxs-lookup"><span data-stu-id="aed33-206">"Print Provider!!\\\\Machine"</span></span><br/>    | <span data-ttu-id="aed33-207">電腦上共用的所有印表機 \\ \\</span><span class="sxs-lookup"><span data-stu-id="aed33-207">All printers shared at \\\\Machine</span></span><br/>                                                     |
| <span data-ttu-id="aed33-208">印表機 \_ 列舉 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="aed33-208">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="aed33-209">空字串 ""</span><span class="sxs-lookup"><span data-stu-id="aed33-209">An empty string, ""</span></span><br/>              | <span data-ttu-id="aed33-210">所有本機印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-210">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="aed33-211">印表機 \_ 列舉 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="aed33-211">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="aed33-212">**NULL**</span><span class="sxs-lookup"><span data-stu-id="aed33-212">**NULL**</span></span><br/>                         | <span data-ttu-id="aed33-213">電腦網域中的所有列印提供者</span><span class="sxs-lookup"><span data-stu-id="aed33-213">All print providers in the computer's domain</span></span><br/>                                           |
| <span data-ttu-id="aed33-214">印表機 \_ 列舉 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="aed33-214">PRINTER\_ENUM\_CONNECTIONS</span></span>                         | <span data-ttu-id="aed33-215">*Name* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="aed33-215">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="aed33-216">所有連線的遠端印表機</span><span class="sxs-lookup"><span data-stu-id="aed33-216">All connected remote printers</span></span><br/>                                                          |
| <span data-ttu-id="aed33-217">印表機 \_ 列舉 \_ 網路</span><span class="sxs-lookup"><span data-stu-id="aed33-217">PRINTER\_ENUM\_NETWORK</span></span>                             | <span data-ttu-id="aed33-218">*Name* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="aed33-218">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="aed33-219">電腦網域中的所有印表機</span><span class="sxs-lookup"><span data-stu-id="aed33-219">All printers in the computer's domain</span></span><br/>                                                  |
| <span data-ttu-id="aed33-220">印表機 \_ 列舉 \_ 遠端</span><span class="sxs-lookup"><span data-stu-id="aed33-220">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="aed33-221">空字串 ""</span><span class="sxs-lookup"><span data-stu-id="aed33-221">An empty string, ""</span></span><br/>              | <span data-ttu-id="aed33-222">電腦網域中的所有印表機和列印伺服器</span><span class="sxs-lookup"><span data-stu-id="aed33-222">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="aed33-223">印表機 \_ 列舉 \_ 遠端</span><span class="sxs-lookup"><span data-stu-id="aed33-223">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="aed33-224">「列印提供者」</span><span class="sxs-lookup"><span data-stu-id="aed33-224">"Print Provider"</span></span><br/>                 | <span data-ttu-id="aed33-225">與印表機 \_ 列舉 \_ 名稱相同</span><span class="sxs-lookup"><span data-stu-id="aed33-225">Same as PRINTER\_ENUM\_NAME</span></span><br/>                                                            |
| <span data-ttu-id="aed33-226">印表機 \_ 列舉 \_ 遠端</span><span class="sxs-lookup"><span data-stu-id="aed33-226">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="aed33-227">「列印提供者！局域</span><span class="sxs-lookup"><span data-stu-id="aed33-227">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="aed33-228">電腦網域中的所有印表機和列印伺服器，不論指定的 *網域* 為何。</span><span class="sxs-lookup"><span data-stu-id="aed33-228">All printers and print servers in computer's domain, regardless of *Domain* specified.</span></span><br/> |
| <span data-ttu-id="aed33-229">印表機 \_ 列舉 \_ 類別 \_ 3d</span><span class="sxs-lookup"><span data-stu-id="aed33-229">PRINTER\_ENUM\_CATEGORY\_3D</span></span>                        | <span data-ttu-id="aed33-230">*Name* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="aed33-230">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="aed33-231">只會列舉3D 印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-231">Only 3D printers are enumerated.</span></span><br/>                                                       |
| <span data-ttu-id="aed33-232">印表機 \_ 列舉 \_ 類別目錄 \_</span><span class="sxs-lookup"><span data-stu-id="aed33-232">PRINTER\_ENUM\_CATEGORY\_ALL</span></span>                       | <span data-ttu-id="aed33-233">*Name* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="aed33-233">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="aed33-234">系統會列舉3D 印表機以及所有其他印表機。</span><span class="sxs-lookup"><span data-stu-id="aed33-234">3D printers are enumerated, along with all other printers.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="aed33-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="aed33-235">Requirements</span></span>



| <span data-ttu-id="aed33-236">需求</span><span class="sxs-lookup"><span data-stu-id="aed33-236">Requirement</span></span> | <span data-ttu-id="aed33-237">值</span><span class="sxs-lookup"><span data-stu-id="aed33-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aed33-238">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aed33-238">Minimum supported client</span></span><br/> | <span data-ttu-id="aed33-239">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aed33-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aed33-240">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aed33-240">Minimum supported server</span></span><br/> | <span data-ttu-id="aed33-241">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aed33-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aed33-242">標頭</span><span class="sxs-lookup"><span data-stu-id="aed33-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed33-243"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="aed33-243"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="aed33-244">程式庫</span><span class="sxs-lookup"><span data-stu-id="aed33-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="aed33-245"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-245"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="aed33-246">DLL</span><span class="sxs-lookup"><span data-stu-id="aed33-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aed33-247"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="aed33-247"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="aed33-248">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="aed33-248">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aed33-249">**EnumPrintersW** (Unicode) 和 **EnumPrintersA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="aed33-249">**EnumPrintersW** (Unicode) and **EnumPrintersA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="aed33-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aed33-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed33-251">列印</span><span class="sxs-lookup"><span data-stu-id="aed33-251">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="aed33-252">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="aed33-252">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="aed33-253">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="aed33-253">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="aed33-254">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="aed33-254">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="aed33-255">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="aed33-255">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="aed33-256">**印表機 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="aed33-256">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="aed33-257">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="aed33-257">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="aed33-258">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="aed33-258">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="aed33-259">**印表機 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="aed33-259">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="aed33-260">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="aed33-260">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

