---
title: COM 錯誤碼的結構
description: COM 錯誤碼的結構
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb27143f50028592f6fe0aeb5cab9795dcd10d4a
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550565"
---
# <a name="structure-of-com-error-codes"></a><span data-ttu-id="dc190-103">COM 錯誤碼的結構</span><span class="sxs-lookup"><span data-stu-id="dc190-103">Structure of COM Error Codes</span></span>

<span data-ttu-id="dc190-104">下圖顯示 [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (或 SCODE) 的格式;數位表示位位置：</span><span class="sxs-lookup"><span data-stu-id="dc190-104">The following illustration shows the format of an [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (or SCODE); the numbers indicate bit positions:</span></span>

![顯示 ' H RESULT ' 或 ' CODE ' 的格式，並以數位表示位位置。](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

<span data-ttu-id="dc190-106">**HRESULT** 或 SCODE 中的高序位位會指出傳回值是否代表成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="dc190-106">The high-order bit in the **HRESULT** or SCODE indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="dc190-107">如果設定為0， \_ 則嚴重性成功，值表示成功。</span><span class="sxs-lookup"><span data-stu-id="dc190-107">If set to 0, SEVERITY\_SUCCESS, the value indicates success.</span></span> <span data-ttu-id="dc190-108">如果設定為1， \_ 則嚴重性錯誤，表示失敗。</span><span class="sxs-lookup"><span data-stu-id="dc190-108">If set to 1, SEVERITY\_ERROR, it indicates failure.</span></span>

<span data-ttu-id="dc190-109">R、C、N 和 r 位是保留的。</span><span class="sxs-lookup"><span data-stu-id="dc190-109">The R, C, N, and r bits are reserved.</span></span>

<span data-ttu-id="dc190-110">[設備] 欄位指出負責錯誤的系統服務。</span><span class="sxs-lookup"><span data-stu-id="dc190-110">The facility field indicates the system service responsible for the error.</span></span> <span data-ttu-id="dc190-111">Microsoft 會在必要時配置新的設施代碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-111">Microsoft allocates new facility codes as they become necessary.</span></span> <span data-ttu-id="dc190-112">大部分的 SCODEs 和 **HRESULT** 值會將設備欄位設定為設備 \_ ITF，表示介面方法錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc190-112">Most SCODEs and **HRESULT** values set the facility field to FACILITY\_ITF, indicating an interface method error.</span></span>

<span data-ttu-id="dc190-113">下表說明常見的設備欄位。</span><span class="sxs-lookup"><span data-stu-id="dc190-113">Common facility fields are described in the following table.</span></span>



| <span data-ttu-id="dc190-114">設備欄位</span><span class="sxs-lookup"><span data-stu-id="dc190-114">Facility Field</span></span>                | <span data-ttu-id="dc190-115">值</span><span class="sxs-lookup"><span data-stu-id="dc190-115">Value</span></span>        | <span data-ttu-id="dc190-116">描述</span><span class="sxs-lookup"><span data-stu-id="dc190-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc190-117">設備 \_ 分派</span><span class="sxs-lookup"><span data-stu-id="dc190-117">FACILITY\_DISPATCH</span></span><br/> | <span data-ttu-id="dc190-118">2</span><span class="sxs-lookup"><span data-stu-id="dc190-118">2</span></span><br/> | <span data-ttu-id="dc190-119">針對晚期繫結的 **IDispatch** 介面錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc190-119">For late-binding **IDispatch** interface errors.</span></span> <br/>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="dc190-120">設施 \_ ITF</span><span class="sxs-lookup"><span data-stu-id="dc190-120">FACILITY\_ITF</span></span><br/>      | <span data-ttu-id="dc190-121">4</span><span class="sxs-lookup"><span data-stu-id="dc190-121">4</span></span><br/> | <span data-ttu-id="dc190-122">針對從介面方法傳回的大部分狀態碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-122">For most status codes returned from interface methods.</span></span> <span data-ttu-id="dc190-123">此錯誤的實際意義是由介面所定義。</span><span class="sxs-lookup"><span data-stu-id="dc190-123">The actual meaning of the error is defined by the interface.</span></span> <span data-ttu-id="dc190-124">也就是說，兩個 **HRESULT**（具有完全相同的32位值，從兩個不同的介面傳回）可能會有不同的意義。</span><span class="sxs-lookup"><span data-stu-id="dc190-124">That is, two **HRESULT** s with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span> <br/>                                                       |
| <span data-ttu-id="dc190-125">設備 \_ Null</span><span class="sxs-lookup"><span data-stu-id="dc190-125">FACILITY\_NULL</span></span><br/>     | <span data-ttu-id="dc190-126">0</span><span class="sxs-lookup"><span data-stu-id="dc190-126">0</span></span><br/> | <span data-ttu-id="dc190-127">適用于廣泛適用的常見狀態碼，例如 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="dc190-127">For broadly applicable common status codes such as S\_OK.</span></span> <br/>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="dc190-128">設備 \_ RPC</span><span class="sxs-lookup"><span data-stu-id="dc190-128">FACILITY\_RPC</span></span><br/>      | <span data-ttu-id="dc190-129">1</span><span class="sxs-lookup"><span data-stu-id="dc190-129">1</span></span><br/> | <span data-ttu-id="dc190-130">適用于遠端程序呼叫所傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-130">For status codes returned from remote procedure calls.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="dc190-131">設備 \_ 存放區</span><span class="sxs-lookup"><span data-stu-id="dc190-131">FACILITY\_STORAGE</span></span><br/>  | <span data-ttu-id="dc190-132">3</span><span class="sxs-lookup"><span data-stu-id="dc190-132">3</span></span><br/> | <span data-ttu-id="dc190-133">針對與結構化儲存相關的 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 方法呼叫所傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-133">For status codes returned from [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) method calls relating to structured storage.</span></span> <span data-ttu-id="dc190-134">其程式碼 (較低16位) 值的狀態碼是在 MS-DOS 錯誤碼的範圍內 (也就是說，小於 256) 與對應的 MS-DOS 錯誤具有相同的意義。</span><span class="sxs-lookup"><span data-stu-id="dc190-134">Status codes whose code (lower 16 bits) value is in the range of MS-DOS error codes (that is, less than 256) have the same meaning as the corresponding MS-DOS error.</span></span> <br/> |
| <span data-ttu-id="dc190-135">設備 \_ WIN32</span><span class="sxs-lookup"><span data-stu-id="dc190-135">FACILITY\_WIN32</span></span><br/>    | <span data-ttu-id="dc190-136">7</span><span class="sxs-lookup"><span data-stu-id="dc190-136">7</span></span><br/> | <span data-ttu-id="dc190-137">用來提供一種方法，從 Windows API 中的函式以 **HRESULT** 的形式處理錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-137">Used to provide a means of handling error codes from functions in the Windows API as an **HRESULT**.</span></span> <span data-ttu-id="dc190-138">16位 OLE 中的錯誤碼也已變更為 [設備 \_ WIN32]。</span><span class="sxs-lookup"><span data-stu-id="dc190-138">Error codes in 16-bit OLE that duplicated system error codes have also been changed to FACILITY\_WIN32.</span></span> <br/>                                                                                                 |
| <span data-ttu-id="dc190-139">設備 \_ 視窗</span><span class="sxs-lookup"><span data-stu-id="dc190-139">FACILITY\_WINDOWS</span></span><br/>  | <span data-ttu-id="dc190-140">8</span><span class="sxs-lookup"><span data-stu-id="dc190-140">8</span></span><br/> | <span data-ttu-id="dc190-141">用於 Microsoft 定義介面中的其他錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-141">Used for additional error codes from Microsoft-defined interfaces.</span></span><br/>                                                                                                                                                                                                                                            |



 

<span data-ttu-id="dc190-142">[程式碼] 欄位是指派來代表錯誤或警告的唯一數位。</span><span class="sxs-lookup"><span data-stu-id="dc190-142">The code field is a unique number that is assigned to represent the error or warning.</span></span>

<span data-ttu-id="dc190-143">依照慣例， **HRESULT** 值通常具有下列格式的名稱：*設備* \_ *嚴重性* \_ *原因*。</span><span class="sxs-lookup"><span data-stu-id="dc190-143">By convention, **HRESULT** values generally have names in the following format: *Facility*\_*Severity*\_*Reason*.</span></span>

<span data-ttu-id="dc190-144">*設備* 可以是設施名稱或其他一些辨別的識別碼; *嚴重性* 是單一字母、S 或 E，表示函式呼叫是否成功 (S) 或產生錯誤 (E) ; *原因* 是描述程式碼意義的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-144">*Facility* is either the facility name or some other distinguishing identifier; *Severity* is a single letter, S or E, that indicates whether the function call succeeded (S) or produced an error (E); and *Reason* is an identifier that describes the meaning of the code.</span></span> <span data-ttu-id="dc190-145">例如，狀態碼 STG. \_ E \_ FILENOTFOUND 指出發生儲存體相關的錯誤，特別是要求的檔案不存在。</span><span class="sxs-lookup"><span data-stu-id="dc190-145">For example, the status code STG\_E\_FILENOTFOUND indicates a storage-related error has occurred; specifically, a requested file does not exist.</span></span> <span data-ttu-id="dc190-146">來自設備的狀態碼 \_ Null 會省略 *設備* \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="dc190-146">Status codes from FACILITY\_NULL omit the *Facility*\_ prefix.</span></span>

<span data-ttu-id="dc190-147">錯誤碼是在介面執行的內容中定義。</span><span class="sxs-lookup"><span data-stu-id="dc190-147">Error codes are defined within the context of an interface implementation.</span></span> <span data-ttu-id="dc190-148">一旦定義之後，就無法變更成功碼或加入新的成功碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-148">Once defined, success codes cannot be changed or new success codes added.</span></span> <span data-ttu-id="dc190-149">不過，您可以撰寫新的失敗代碼。</span><span class="sxs-lookup"><span data-stu-id="dc190-149">However, new failure codes can be written.</span></span> <span data-ttu-id="dc190-150">Microsoft 保留為設備 \_ ITF 或新設施中所述的介面，定義新的失敗碼 (但不是成功碼) 的權利。</span><span class="sxs-lookup"><span data-stu-id="dc190-150">Microsoft reserves the right to define new failure codes (but not success codes) for the interfaces described in FACILITY\_ITF or in new facilities.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc190-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc190-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc190-152">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="dc190-152">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="dc190-153">Windows 通訊協定： HRESULT</span><span class="sxs-lookup"><span data-stu-id="dc190-153">Windows Protocols: HRESULT</span></span>](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

