---
description: AttachProperties 匯出函式會將屬性對應到一段辨識的資料中的位置。 AttachProperties 必須針對剖析器 DLL 支援的每個剖析器來執行。
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: 'AttachProperties 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974261"
---
# <a name="attachproperties-callback-function"></a><span data-ttu-id="5bd48-104">AttachProperties 回呼函式</span><span class="sxs-lookup"><span data-stu-id="5bd48-104">AttachProperties callback function</span></span>

<span data-ttu-id="5bd48-105">**AttachProperties** 匯出函式會將屬性對應到一段辨識的資料中的位置。</span><span class="sxs-lookup"><span data-stu-id="5bd48-105">The **AttachProperties** export function maps the properties to a location within a piece of recognized data.</span></span> <span data-ttu-id="5bd48-106">**AttachProperties** 必須針對剖析器 DLL 支援的每個剖析器來執行。</span><span class="sxs-lookup"><span data-stu-id="5bd48-106">**AttachProperties** must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd48-107">語法</span><span class="sxs-lookup"><span data-stu-id="5bd48-107">Syntax</span></span>


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="5bd48-108">參數</span><span class="sxs-lookup"><span data-stu-id="5bd48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd48-109">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-110">正在剖析之框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5bd48-110">Handle of the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="5bd48-111">*lpFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-112">框架中第一個位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="5bd48-112">Pointer to the first byte in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="5bd48-113">*lpProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-114">已辨識資料開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="5bd48-114">Pointer to the start of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="5bd48-115">*MacType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-115">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-116">框架中第一個通訊協定的 MAC 值。</span><span class="sxs-lookup"><span data-stu-id="5bd48-116">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="5bd48-117">*MacType* 可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="5bd48-117">The *MacType* can be one of the following:</span></span>



| <span data-ttu-id="5bd48-118">值</span><span class="sxs-lookup"><span data-stu-id="5bd48-118">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="5bd48-119">意義</span><span class="sxs-lookup"><span data-stu-id="5bd48-119">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="5bd48-120"><dt>**MAC \_ 類型 \_ ETHERNET**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd48-120"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="5bd48-121">802.3</span><span class="sxs-lookup"><span data-stu-id="5bd48-121">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="5bd48-122"><dt>**MAC \_ 類型 \_ TOKENRING**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd48-122"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="5bd48-123">802.5</span><span class="sxs-lookup"><span data-stu-id="5bd48-123">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="5bd48-124"><dt>**MAC \_ 類型的 \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd48-124"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="5bd48-125">ANSI X3T 9。5</span><span class="sxs-lookup"><span data-stu-id="5bd48-125">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="5bd48-126">*BytesLeft* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-126">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-127">框架中剩餘的位元組數目，從已辨識的資料開頭開始。</span><span class="sxs-lookup"><span data-stu-id="5bd48-127">The remaining number of bytes in a frame   starting at the beginning of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="5bd48-128">*hPreviousProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-128">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-129">先前通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5bd48-129">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5bd48-130">*nPreviousProtocolOffset* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-130">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-131">先前的通訊協定從框架開頭開始的位移。</span><span class="sxs-lookup"><span data-stu-id="5bd48-131">Offset of the previous protocol   starting at the beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="5bd48-132">*lpInstData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-132">*lpInstData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd48-133">先前的通訊協定所提供之實例資料的指標。</span><span class="sxs-lookup"><span data-stu-id="5bd48-133">Pointer to the instance data that the previous protocol provides.</span></span> <span data-ttu-id="5bd48-134">實例資料的長度不能超過 DWORD \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="5bd48-134">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd48-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bd48-135">Return value</span></span>

<span data-ttu-id="5bd48-136">如果函式成功，則傳回值為框架中已辨識資料之後第一個位元組的指標，如果可辨識的資料是框架中的最後一個資料片段，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5bd48-136">If the function is successful, the return value is a pointer to the first byte after the recognized data in a frame or **NULL** if the recognized data is the last piece of data in a frame.</span></span>

<span data-ttu-id="5bd48-137">如果函式不成功，則傳回值會是已辨識資料的指標。</span><span class="sxs-lookup"><span data-stu-id="5bd48-137">If the function is unsuccessful, the return value is a pointer to the recognized data.</span></span> <span data-ttu-id="5bd48-138">*LpProtocol* 參數會將指標傳遞至剖析器 DLL。</span><span class="sxs-lookup"><span data-stu-id="5bd48-138">The *lpProtocol* parameter passes the pointer to the parser DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd48-139">備註</span><span class="sxs-lookup"><span data-stu-id="5bd48-139">Remarks</span></span>

<span data-ttu-id="5bd48-140">網路監視器會針對辨識框架中某部分資料的每個剖析器，呼叫 **AttachProperties** 函數。</span><span class="sxs-lookup"><span data-stu-id="5bd48-140">Network Monitor calls the **AttachProperties** function for each parser that recognizes a piece of data in a frame.</span></span> <span data-ttu-id="5bd48-141">請注意，剖析器會判斷哪些屬性存在於已辨識的資料中，以及每個屬性的所在位置。</span><span class="sxs-lookup"><span data-stu-id="5bd48-141">Note that the parser determines which properties exist in the recognized data, and where each property is located.</span></span>

<span data-ttu-id="5bd48-142">在 **AttachProperties** 的執行期間，呼叫 [AttachPropertyInstance](attachpropertyinstance.md) 以使用存在於捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="5bd48-142">During the implementation of **AttachProperties**, call [AttachPropertyInstance](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="5bd48-143">您也可以呼叫 [AttachPropertyInstanceEx](attachpropertyinstanceex.md) 函數來修改屬性資料。</span><span class="sxs-lookup"><span data-stu-id="5bd48-143">You can also call [AttachPropertyInstanceEx](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="5bd48-144">不過，建議您使用存在於捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="5bd48-144">However, it is advised that you use the data as it exists in the capture.</span></span>

<span data-ttu-id="5bd48-145">**AttachPropertyInstanceEx** 和 **AttachPropertyInstance** 函式只會針對存在於已辨識資料中的屬性進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="5bd48-145">The **AttachPropertyInstanceEx** and **AttachPropertyInstance** functions are called only for the properties that exist in the recognized data.</span></span> <span data-ttu-id="5bd48-146">請注意，網路監視器具有剖析器的 [*屬性資料庫*](p.md) ，其中包含剖析器所支援之所有屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="5bd48-146">Note that Network Monitor has a [*property database*](p.md) for the parser that contains a description of all the properties that the parser supports.</span></span>

<span data-ttu-id="5bd48-147">**執行個體資料**</span><span class="sxs-lookup"><span data-stu-id="5bd48-147">**Instance data**</span></span>

<span data-ttu-id="5bd48-148">實例資料是從某個剖析器傳遞至另一個剖析器的資訊。</span><span class="sxs-lookup"><span data-stu-id="5bd48-148">Instance data is information that is passed from one parser to another.</span></span> <span data-ttu-id="5bd48-149">實例資料可以是小於或等於 DWORD 指標長度的任何資料，或是不需要由剖析器配置 \_ 或釋放的資料指標，例如原始框架資料。</span><span class="sxs-lookup"><span data-stu-id="5bd48-149">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span> <span data-ttu-id="5bd48-150">在 **AttachProperties** 和 [RecognizeFrame](recognizeframe.md)函式的 *lpInstData* 參數中，網路監視器提供上一個通訊協定的實例資料指標。</span><span class="sxs-lookup"><span data-stu-id="5bd48-150">In the *lpInstData* parameter of the **AttachProperties** and [RecognizeFrame](recognizeframe.md) functions, Network Monitor provides a pointer to the instance data of the previous protocol.</span></span> <span data-ttu-id="5bd48-151">您可以在 **RecognizeFrame** 的執行期間，設定剖析器的實例資料。</span><span class="sxs-lookup"><span data-stu-id="5bd48-151">You can set the instance data for your parser during your implementation of **RecognizeFrame**.</span></span>



| <span data-ttu-id="5bd48-152">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="5bd48-152">For information on</span></span>                                          | <span data-ttu-id="5bd48-153">請參閱</span><span class="sxs-lookup"><span data-stu-id="5bd48-153">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5bd48-154">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="5bd48-154">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="5bd48-155">解析 器</span><span class="sxs-lookup"><span data-stu-id="5bd48-155">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="5bd48-156">剖析器 DLL 中包含了哪些進入點。</span><span class="sxs-lookup"><span data-stu-id="5bd48-156">What entry points are included in the parser DLL.</span></span>           | [<span data-ttu-id="5bd48-157">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="5bd48-157">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="5bd48-158">如何辨識資料。</span><span class="sxs-lookup"><span data-stu-id="5bd48-158">How to recognize data.</span></span>                                      | [<span data-ttu-id="5bd48-159">執行 RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="5bd48-159">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)     |
| <span data-ttu-id="5bd48-160">如何建立屬性資料庫。</span><span class="sxs-lookup"><span data-stu-id="5bd48-160">How to create a property database.</span></span>                          | [<span data-ttu-id="5bd48-161">執行註冊</span><span class="sxs-lookup"><span data-stu-id="5bd48-161">Implementing Register</span></span>](implementing-register.md)                 |
| <span data-ttu-id="5bd48-162">如何執行 **AttachProperties**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="5bd48-162">How to implement **AttachProperties**  includes an example.</span></span> | [<span data-ttu-id="5bd48-163">執行 AttachProperties</span><span class="sxs-lookup"><span data-stu-id="5bd48-163">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="5bd48-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bd48-164">Requirements</span></span>



| <span data-ttu-id="5bd48-165">需求</span><span class="sxs-lookup"><span data-stu-id="5bd48-165">Requirement</span></span> | <span data-ttu-id="5bd48-166">值</span><span class="sxs-lookup"><span data-stu-id="5bd48-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd48-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bd48-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd48-168">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5bd48-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bd48-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd48-170">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bd48-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5bd48-171">標頭</span><span class="sxs-lookup"><span data-stu-id="5bd48-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bd48-172"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="5bd48-172"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd48-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bd48-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd48-174">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="5bd48-174">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="5bd48-175">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="5bd48-175">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="5bd48-176">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="5bd48-176">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




