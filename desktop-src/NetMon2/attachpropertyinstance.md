---
description: AttachPropertyInstance 函式會將現有的屬性對應到可辨識資料中的特定位置。
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: 'AttachPropertyInstance 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850915"
---
# <a name="attachpropertyinstance-function"></a><span data-ttu-id="d92b7-103">AttachPropertyInstance 函式</span><span class="sxs-lookup"><span data-stu-id="d92b7-103">AttachPropertyInstance function</span></span>

<span data-ttu-id="d92b7-104">**AttachPropertyInstance** 函式會將現有的屬性對應到可辨識資料中的特定位置。</span><span class="sxs-lookup"><span data-stu-id="d92b7-104">The **AttachPropertyInstance** function maps an existing property to a specific location in the recognized data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="d92b7-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d92b7-106">參數</span><span class="sxs-lookup"><span data-stu-id="d92b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d92b7-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b7-108">要剖析之框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d92b7-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="d92b7-109">在 [**AttachProperties**](attachproperties.md)函數的 *hFrame* 參數中，使用傳遞至剖析器 DLL 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d92b7-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d92b7-110">*hProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b7-111">定義屬性之 [**PROPERTYINFO**](propertyinfo.md) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d92b7-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="d92b7-112">當您執行 [**Register**](register-parser.md) export 函式時，您會指定定義屬性的 **PROPERTYINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="d92b7-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="d92b7-113">*長度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b7-114">這個屬性實例的資料長度。</span><span class="sxs-lookup"><span data-stu-id="d92b7-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="d92b7-115">*lpData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b7-116">可辨識的資料中，屬性值所在位置的指標。</span><span class="sxs-lookup"><span data-stu-id="d92b7-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="d92b7-117">在 [**AttachProperties**](attachproperties.md)函數的 *lpProtocol* 參數中，使用傳遞至剖析器 DLL 的指標。</span><span class="sxs-lookup"><span data-stu-id="d92b7-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d92b7-118">*H* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-118">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b7-119">識別碼 (從0到 2047) 用來設定屬性的即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="d92b7-119">Identifier (from 0 to 2047) used to set context-sensitive Help for the property.</span></span>

<span data-ttu-id="d92b7-120">識別碼是相對於與通訊協定 [*屬性資料庫*](p.md)相關聯的說明檔。</span><span class="sxs-lookup"><span data-stu-id="d92b7-120">The identifier number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="d92b7-121">*IndentLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-121">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b7-122">縮排層級 (從0到 15) 用來以階層方式顯示內容。</span><span class="sxs-lookup"><span data-stu-id="d92b7-122">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="d92b7-123">網路監視器使用層級0到14來縮排屬性。</span><span class="sxs-lookup"><span data-stu-id="d92b7-123">Network Monitor uses levels 0 through 14 to indent properties.</span></span> <span data-ttu-id="d92b7-124">層級15是特殊值，可讓剖析器附加不可見的隱藏屬性。</span><span class="sxs-lookup"><span data-stu-id="d92b7-124">Level 15 is a special value that allows a parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="d92b7-125">*IFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-125">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b7-126">位域值，指出位在屬性中的順序。</span><span class="sxs-lookup"><span data-stu-id="d92b7-126">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="d92b7-127">將 *fError* 設定為0或1的先前剖析器，現在應該將 *FERROR* 設定為 IFLAG \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="d92b7-127">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="d92b7-128">將此參數設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d92b7-128">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="d92b7-129">值</span><span class="sxs-lookup"><span data-stu-id="d92b7-129">Value</span></span>                                                                                                                                                         | <span data-ttu-id="d92b7-130">意義</span><span class="sxs-lookup"><span data-stu-id="d92b7-130">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="d92b7-131"><dt>**IFLAG \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="d92b7-131"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="d92b7-132">框架中的資料發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d92b7-132">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="d92b7-133"><dt>**IFLAG \_ 交換**</dt></span><span class="sxs-lookup"><span data-stu-id="d92b7-133"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="d92b7-134">在附加時， **文字** 位元組是非 Intel 格式。</span><span class="sxs-lookup"><span data-stu-id="d92b7-134">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="d92b7-135"><dt>**IFLAG \_ UNICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="d92b7-135"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="d92b7-136">在附加時間， **字串** 是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="d92b7-136">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d92b7-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="d92b7-137">Return value</span></span>

<span data-ttu-id="d92b7-138">如果函式成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d92b7-138">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="d92b7-139">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d92b7-139">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92b7-140">備註</span><span class="sxs-lookup"><span data-stu-id="d92b7-140">Remarks</span></span>

<span data-ttu-id="d92b7-141">**AttachPropertyInstance** 函式會在 [**AttachProperties**](attachproperties.md)匯出函數的執行期間呼叫。</span><span class="sxs-lookup"><span data-stu-id="d92b7-141">The **AttachPropertyInstance** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="d92b7-142">當屬性附加至資料時，網路監視器會建立 [**PROPERTYINST**](propertyinst.md) 結構，以定義附加屬性的實例。</span><span class="sxs-lookup"><span data-stu-id="d92b7-142">When a property is attached to the data, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property.</span></span>

<span data-ttu-id="d92b7-143">在 [**AttachProperties**](attachproperties.md)的執行期間，呼叫 **AttachPropertyInstance** 以使用存在於捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="d92b7-143">During the implementation of [**AttachProperties**](attachproperties.md), call **AttachPropertyInstance** to use the data as it exists in the capture.</span></span> <span data-ttu-id="d92b7-144">您也可以呼叫 [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) 函數來修改屬性資料。</span><span class="sxs-lookup"><span data-stu-id="d92b7-144">You can also call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="d92b7-145">不過，建議您使用存在於捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="d92b7-145">However, it is advised that you use the data as it exists in the capture.</span></span>



| <span data-ttu-id="d92b7-146">的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d92b7-146">For Information on</span></span>                                        | <span data-ttu-id="d92b7-147">請參閱</span><span class="sxs-lookup"><span data-stu-id="d92b7-147">See</span></span>                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d92b7-148">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="d92b7-148">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="d92b7-149">**解析 器**</span><span class="sxs-lookup"><span data-stu-id="d92b7-149">**Parsers**</span></span>](parsers.md)                                         |
| <span data-ttu-id="d92b7-150">如何呼叫 **AttachPropertyInstance**。</span><span class="sxs-lookup"><span data-stu-id="d92b7-150">How to call **AttachPropertyInstance**.</span></span>                   | [<span data-ttu-id="d92b7-151">執行 AttachProperties</span><span class="sxs-lookup"><span data-stu-id="d92b7-151">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="d92b7-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="d92b7-152">Requirements</span></span>



| <span data-ttu-id="d92b7-153">需求</span><span class="sxs-lookup"><span data-stu-id="d92b7-153">Requirement</span></span> | <span data-ttu-id="d92b7-154">值</span><span class="sxs-lookup"><span data-stu-id="d92b7-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d92b7-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d92b7-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d92b7-156">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d92b7-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d92b7-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d92b7-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d92b7-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d92b7-159">標頭</span><span class="sxs-lookup"><span data-stu-id="d92b7-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="d92b7-160"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="d92b7-160"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d92b7-161">程式庫</span><span class="sxs-lookup"><span data-stu-id="d92b7-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="d92b7-162"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d92b7-162"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d92b7-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d92b7-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d92b7-164"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d92b7-164"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d92b7-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d92b7-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92b7-166">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="d92b7-166">**AttachProperties**</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="d92b7-167">**AttachPropertyInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="d92b7-167">**AttachPropertyInstanceEx**</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="d92b7-168">**PROPERTYINST**</span><span class="sxs-lookup"><span data-stu-id="d92b7-168">**PROPERTYINST**</span></span>](propertyinst.md)
</dt> </dl>

 

 




