---
description: RecognizeFrame export 函數會指出是否要將資料片段辨識為剖析器偵測到的通訊協定。 必須針對剖析器 DLL 支援的每個剖析器，執行 RecognizeFrame 匯出函數。
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: 'RecognizeFrame 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986627"
---
# <a name="recognizeframe-callback-function"></a><span data-ttu-id="0b3fd-104">RecognizeFrame 回呼函式</span><span class="sxs-lookup"><span data-stu-id="0b3fd-104">RecognizeFrame callback function</span></span>

<span data-ttu-id="0b3fd-105">**RecognizeFrame** export 函數會指出是否要將資料片段辨識為剖析器偵測到的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-105">The **RecognizeFrame** export function indicates whether a piece of data is recognized as the protocol that the parser detects.</span></span> <span data-ttu-id="0b3fd-106">必須針對剖析器 DLL 支援的每個剖析器，執行 **RecognizeFrame** 匯出函數。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-106">The **RecognizeFrame** export function must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3fd-107">語法</span><span class="sxs-lookup"><span data-stu-id="0b3fd-107">Syntax</span></span>


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="0b3fd-108">參數</span><span class="sxs-lookup"><span data-stu-id="0b3fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b3fd-109">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-110">包含資料之框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-110">Handle to the frame that contains the data.</span></span>

</dd> <dt>

<span data-ttu-id="0b3fd-111">*lpFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-112">框架第一個位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-112">Pointer to the first byte of a frame.</span></span> <span data-ttu-id="0b3fd-113">指標會提供一種方式來查看其他剖析器辨識的資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-113">The pointer provides a way to view data that other parsers recognize.</span></span>

</dd> <dt>

<span data-ttu-id="0b3fd-114">*lpProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-114">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-115">取消認領資料開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-115">Pointer to the start of the unclaimed data.</span></span> <span data-ttu-id="0b3fd-116">一般而言，取消認領資料是位於框架的中間，因為先前的剖析器已在此剖析器之前宣告資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-116">Typically, the unclaimed data is located in the middle of a frame because a previous parser has claimed data before this parser.</span></span> <span data-ttu-id="0b3fd-117">剖析器必須先測試取消認領的資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-117">The parser must test the unclaimed data first.</span></span>

</dd> <dt>

<span data-ttu-id="0b3fd-118">*MacType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-118">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-119">框架中第一個通訊協定的 MAC 值。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-119">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="0b3fd-120">一般來說，當剖析器必須識別框架中的第一個通訊協定時，就會使用 *MacType* 值。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-120">Typically, the *MacType* value is used when the parser must identify the first protocol in a frame.</span></span> <span data-ttu-id="0b3fd-121">*MacType* 值可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="0b3fd-121">The *MacType* value can be one of the following:</span></span>



| <span data-ttu-id="0b3fd-122">值</span><span class="sxs-lookup"><span data-stu-id="0b3fd-122">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="0b3fd-123">意義</span><span class="sxs-lookup"><span data-stu-id="0b3fd-123">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="0b3fd-124"><dt>**MAC \_ 類型 \_ ETHERNET**</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-124"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="0b3fd-125">802.3</span><span class="sxs-lookup"><span data-stu-id="0b3fd-125">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="0b3fd-126"><dt>**MAC \_ 類型 \_ TOKENRING**</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-126"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="0b3fd-127">802.5</span><span class="sxs-lookup"><span data-stu-id="0b3fd-127">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="0b3fd-128"><dt>**MAC \_ 類型的 \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-128"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="0b3fd-129">ANSI X3T 9。5</span><span class="sxs-lookup"><span data-stu-id="0b3fd-129">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="0b3fd-130">*BytesLeft* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-130">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-131">從框架位置到框架結尾的剩餘位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-131">The remaining number of bytes from a location in a frame to the end of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="0b3fd-132">*hPreviousProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-132">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-133">先前通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-133">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0b3fd-134">*nPreviousProtocolOffset* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-134">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-135">框架開頭的先前通訊協定位移。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-135">Offset of the previous protocol   beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="0b3fd-136">*ProtocolStatusCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-136">*ProtocolStatusCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-137">通訊協定狀態指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-137">Protocol status indicator.</span></span> <span data-ttu-id="0b3fd-138">剖析器 DLL 必須設定下列其中一個狀態碼。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-138">The parser DLL must set one of the following status codes.</span></span>



| <span data-ttu-id="0b3fd-139">值</span><span class="sxs-lookup"><span data-stu-id="0b3fd-139">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="0b3fd-140">意義</span><span class="sxs-lookup"><span data-stu-id="0b3fd-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <span data-ttu-id="0b3fd-141"><dt>**識別的通訊協定 \_ 狀態 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-141"><dt>**PROTOCOL\_STATUS\_RECOGNIZED**</dt></span></span> </dl>              | <span data-ttu-id="0b3fd-142">剖析器會辨識資料，但不知道接下來的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-142">The parser recognizes the data but does not know which protocol follows.</span></span> <span data-ttu-id="0b3fd-143">設定完程式碼之後，請將指標傳回至遵循辨識通訊協定的其餘取消認領資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-143">After setting the code, return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="0b3fd-144">網路監視器會使用 [*下列一組*](f.md) 通訊協定來繼續剖析。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-144">Network Monitor uses the [*follow set*](f.md) of the protocol to continue parsing.</span></span> <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <span data-ttu-id="0b3fd-145"><dt>**無法辨識通訊協定 \_ 狀態 \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-145"><dt>**PROTOCOL\_STATUS\_NOT\_RECOGNIZED**</dt></span></span> </dl> | <span data-ttu-id="0b3fd-146">剖析器無法辨識資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-146">The parser does not recognize the data.</span></span> <span data-ttu-id="0b3fd-147">設定此程式碼之後，請使用 *lpProtocol* 參數傳遞至剖析器 DLL 的指標，將指標傳回至資料的開頭。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-147">After setting this code, return the pointer to the beginning of the data   using the pointer that the *lpProtocol* parameter passes to the parser DLL.</span></span> <span data-ttu-id="0b3fd-148">網路監視器使用先前的通訊協定 *集合* 來繼續剖析。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-148">Network Monitor uses the *follow set* of the previous protocol to continue parsing.</span></span> <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <span data-ttu-id="0b3fd-149"><dt>**已宣告的通訊協定 \_ 狀態 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-149"><dt>**PROTOCOL\_STATUS\_CLAIMED**</dt></span></span> </dl>                       | <span data-ttu-id="0b3fd-150">剖析器會辨識資料並宣告剩餘的資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-150">The parser recognizes the data and claims the remaining data.</span></span> <span data-ttu-id="0b3fd-151">設定程式碼之後，請針對網路監視器傳回 **Null** ，以終止剖析框架。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-151">After setting the code, return **NULL** for Network Monitor to terminate parsing a frame.</span></span> <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <span data-ttu-id="0b3fd-152"><dt>**通訊協定 \_ 狀態 \_ 下一個 \_ 通訊協定**</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-152"><dt>**PROTOCOL\_STATUS\_NEXT\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="0b3fd-153">剖析器會辨識資料並知道接下來的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-153">The parser recognizes the data and knows which protocol follows.</span></span> <span data-ttu-id="0b3fd-154">設定程式碼之後，請設定 *phNextProtocol* 參數，並將指標傳回其餘的取消認領資料，並遵循辨識的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-154">After setting the code, set the *phNextProtocol* parameter, and return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="0b3fd-155">網路監視器會繼續剖析框架。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-155">Network Monitor continues parsing the frame.</span></span> <br/>                               |



 

</dd> <dt>

<span data-ttu-id="0b3fd-156">*phNextProtocol* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-156">*phNextProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-157">下一個通訊協定的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-157">Pointer to the handle of the next protocol.</span></span> <span data-ttu-id="0b3fd-158">當通訊協定識別遵循通訊協定的通訊協定時，就會設定此參數。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-158">This parameter is set when a protocol identifies the protocol that follows a protocol.</span></span> <span data-ttu-id="0b3fd-159">若要取得下一個通訊協定的控制碼，請呼叫 [GetProtocolFromTable](getprotocolfromtable.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-159">To obtain the handle of the next protocol, call the [GetProtocolFromTable](getprotocolfromtable.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0b3fd-160">*lpInstData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-160">*lpInstData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b3fd-161">在輸入上，從先前的通訊協定指向實例資料的指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-161">On input, a pointer to the instance data from the previous protocol.</span></span>

<span data-ttu-id="0b3fd-162">在輸出時，為目前通訊協定的實例資料指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-162">On output, a pointer to the instance data for the current protocol.</span></span> <span data-ttu-id="0b3fd-163">實例資料的長度不能超過 DWORD \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-163">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b3fd-164">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b3fd-164">Return value</span></span>

<span data-ttu-id="0b3fd-165">如果函式成功，則傳回值會是已辨識之剖析器資料之後第一個位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-165">If the function is successful, the return value is a pointer to the first byte after the recognized parser data.</span></span> <span data-ttu-id="0b3fd-166">如果剖析器宣告所有剩餘的資料，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-166">If the parser claims all the remaining data, the return value is **NULL**.</span></span>

<span data-ttu-id="0b3fd-167">如果函式不成功，則傳回值是 *lpProtocol* 參數傳入的初始指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-167">If the function is unsuccessful, the return value is an initial pointer that the *lpProtocol* parameter passes-in.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b3fd-168">備註</span><span class="sxs-lookup"><span data-stu-id="0b3fd-168">Remarks</span></span>

<span data-ttu-id="0b3fd-169">**RecognizeFrame** 函式會判斷剖析器是否從 *lpProtocol* 指標開始識別原始資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-169">The **RecognizeFrame** function determines whether the parser recognizes the raw data   starting at the *lpProtocol* pointer.</span></span>

-   <span data-ttu-id="0b3fd-170">如果通訊協定辨識資料， **RecognizeFrame** 函式會傳回剩餘資料的指標，如果目前的通訊協定是框架中的最後一個通訊協定，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-170">If the protocol recognizes the data, the **RecognizeFrame** function returns a pointer to the remaining data, or returns **NULL** if the current protocol is the last protocol in a frame.</span></span>
-   <span data-ttu-id="0b3fd-171">如果通訊協定無法辨識資料， **RecognizeFrame** 函式會傳回在 *lpProtocol* 參數中傳遞至剖析器 DLL 的指標。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-171">If the protocol does not recognize the data, the **RecognizeFrame** function returns the pointer passed to the parser DLL in the *lpProtocol* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="0b3fd-172">您可以在呼叫 [*register*](register-parser.md)函數之前呼叫 *RecognizeFrame* ，以註冊通訊協定屬性。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-172">*RecognizeFrame* can be called before the [*Register*](register-parser.md) function is called to register the protocol properties.</span></span> <span data-ttu-id="0b3fd-173">基於這個理由， *RecognizeFrame* 函式的執行不依賴在通訊協定 **註冊** 函式執行期間所建立或初始化的任何屬性或結構。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-173">For that reason, the implementation of the *RecognizeFrame* function does not rely on any properties or structures that are created or initialized during the implementation of the protocol **Register** function.</span></span>

 

<span data-ttu-id="0b3fd-174">**交付集和後續設定**</span><span class="sxs-lookup"><span data-stu-id="0b3fd-174">**Handoff Set and Follow Set**</span></span>

<span data-ttu-id="0b3fd-175">剖析器可以使用「認可集」或「設定」（set）來識別網路監視器遵循辨識資料的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-175">A parser can use a handoff set or follow set to identify for Network Monitor the protocol that follows recognized data.</span></span>

-   <span data-ttu-id="0b3fd-176">如果可辨識的資料中有可用的資訊，剖析器會使用它的遞交集來取得下一個通訊協定的控制碼，然後將該控制碼傳遞給網路監視器。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-176">If information is available in recognized data, the parser uses its handoff set to obtain a handle to the next protocol, and then passes that handle to Network Monitor.</span></span>
-   <span data-ttu-id="0b3fd-177">如果資訊無法使用，剖析器不會傳遞控制碼，網路監視器會使用剖析器之後的設定來決定接下來的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-177">If information is not available, the parser does not pass a handle, and Network Monitor uses the parser follow set to determine which protocol follows.</span></span>

<span data-ttu-id="0b3fd-178">**在通訊協定之間傳遞資訊**</span><span class="sxs-lookup"><span data-stu-id="0b3fd-178">**Passing information between protocols**</span></span>

<span data-ttu-id="0b3fd-179">使用 *lpInstData* 參數傳遞通訊協定之間的資訊。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-179">Use the *lpInstData* parameter to pass information between protocols.</span></span> <span data-ttu-id="0b3fd-180">在輸入上，您可以從先前的通訊協定取得資訊。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-180">On input, you can retrieve the information from the previous protocol.</span></span> <span data-ttu-id="0b3fd-181">在輸出中，您可以將資訊傳遞至下一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-181">On output, you can pass information to the next protocol.</span></span>

<span data-ttu-id="0b3fd-182">實例資料可以是小於或等於 DWORD 指標長度的任何資料，或是不需要由剖析器配置 \_ 或釋放的資料指標，例如原始框架資料。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-182">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>



| <span data-ttu-id="0b3fd-183">的相關資訊</span><span class="sxs-lookup"><span data-stu-id="0b3fd-183">For Information on</span></span>                                        | <span data-ttu-id="0b3fd-184">請參閱</span><span class="sxs-lookup"><span data-stu-id="0b3fd-184">See</span></span>                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3fd-185">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-185">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="0b3fd-186">解析 器</span><span class="sxs-lookup"><span data-stu-id="0b3fd-186">Parsers</span></span>](parsers.md)                                                                                                    |
| <span data-ttu-id="0b3fd-187">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-187">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="0b3fd-188">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="0b3fd-188">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                                                                    |
| <span data-ttu-id="0b3fd-189">如何執行 **RecognizeFrame**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-189">How to implement **RecognizeFrame**  includes an example.</span></span> | [<span data-ttu-id="0b3fd-190">執行 RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="0b3fd-190">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)                                                            |
| <span data-ttu-id="0b3fd-191">如何指定遞交集，並遵循 set。</span><span class="sxs-lookup"><span data-stu-id="0b3fd-191">How to specify a handoff set and follow set.</span></span>              | <span data-ttu-id="0b3fd-192">[指定追蹤集](specifying-a-handoff-set.md)[指定追蹤](specifying-a-follow-set.md)集</span><span class="sxs-lookup"><span data-stu-id="0b3fd-192">[Specifying a Handoff Set](specifying-a-handoff-set.md)[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0b3fd-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b3fd-193">Requirements</span></span>



| <span data-ttu-id="0b3fd-194">需求</span><span class="sxs-lookup"><span data-stu-id="0b3fd-194">Requirement</span></span> | <span data-ttu-id="0b3fd-195">值</span><span class="sxs-lookup"><span data-stu-id="0b3fd-195">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3fd-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b3fd-196">Minimum supported client</span></span><br/> | <span data-ttu-id="0b3fd-197">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0b3fd-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b3fd-198">Minimum supported server</span></span><br/> | <span data-ttu-id="0b3fd-199">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b3fd-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0b3fd-200">標頭</span><span class="sxs-lookup"><span data-stu-id="0b3fd-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b3fd-201"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="0b3fd-201"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b3fd-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b3fd-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3fd-203">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="0b3fd-203">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> </dl>

 

 




