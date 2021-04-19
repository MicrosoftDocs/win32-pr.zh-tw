---
description: AttachPropertyInstanceEx 函式會將現有的屬性對應至已辨識資料中的特定位置，並修改屬性資料的值。
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: 'AttachPropertyInstanceEx 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989389"
---
# <a name="attachpropertyinstanceex-function"></a><span data-ttu-id="41638-103">AttachPropertyInstanceEx 函式</span><span class="sxs-lookup"><span data-stu-id="41638-103">AttachPropertyInstanceEx function</span></span>

<span data-ttu-id="41638-104">**AttachPropertyInstanceEx** 函式會將現有的屬性對應至已辨識資料中的特定位置，並修改屬性資料的值。</span><span class="sxs-lookup"><span data-stu-id="41638-104">The **AttachPropertyInstanceEx** function maps an existing property to a specific location in the recognized data, and modifies the value of the property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="41638-105">語法</span><span class="sxs-lookup"><span data-stu-id="41638-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="41638-106">參數</span><span class="sxs-lookup"><span data-stu-id="41638-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41638-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-108">要剖析之框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="41638-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="41638-109">在 [**AttachProperties**](attachproperties.md)函數的 *hFrame* 參數中，使用傳遞至剖析器 DLL 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="41638-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="41638-110">*hProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-111">定義屬性之 [**PROPERTYINFO**](propertyinfo.md) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="41638-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="41638-112">當您執行 [**Register**](register-parser.md) export 函式時，您會指定定義屬性的 **PROPERTYINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="41638-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="41638-113">*長度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-114">這個屬性實例的資料長度。</span><span class="sxs-lookup"><span data-stu-id="41638-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="41638-115">*lpData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-116">可辨識的資料中，屬性值所在位置的指標。</span><span class="sxs-lookup"><span data-stu-id="41638-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="41638-117">在 [**AttachProperties**](attachproperties.md)函數的 *lpProtocol* 參數中，使用傳遞至剖析器 DLL 的指標。</span><span class="sxs-lookup"><span data-stu-id="41638-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="41638-118">*LengthEx* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-118">*LengthEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-119">擴充資料長度的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="41638-119">Length of the extended data   length in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="41638-120">*lpDataEx* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-120">*lpDataEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-121">擴充資料的指標，通常是包含擴充資料的堆疊變數。</span><span class="sxs-lookup"><span data-stu-id="41638-121">Pointer to the extended data, which is typically a stack variable that contains the extend data.</span></span>

</dd> <dt>

<span data-ttu-id="41638-122">*H* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-122">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-123">識別碼 (從0到 2047) 用來設定屬性的即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="41638-123">Identifier (from 0 to 2047) used to set context-sensitive Help for a property.</span></span>

<span data-ttu-id="41638-124">*H* 號碼相對於與通訊協定 [*屬性資料庫*](p.md)相關聯的說明檔。</span><span class="sxs-lookup"><span data-stu-id="41638-124">The *HelpID* number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="41638-125">*IndentLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-125">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-126">縮排層級 (從0到 15) 用來以階層方式顯示內容。</span><span class="sxs-lookup"><span data-stu-id="41638-126">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="41638-127">網路監視器使用層級0到9。</span><span class="sxs-lookup"><span data-stu-id="41638-127">Network Monitor uses levels 0 through 9.</span></span> <span data-ttu-id="41638-128">層級15是特殊值，可讓剖析器附加不可見的隱藏屬性。</span><span class="sxs-lookup"><span data-stu-id="41638-128">Level 15 is a special value that allows the parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="41638-129">*IFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41638-129">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41638-130">位域值，指出位在屬性中的順序。</span><span class="sxs-lookup"><span data-stu-id="41638-130">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="41638-131">將 *fError* 設定為0或1的先前剖析器，現在應該將 *FERROR* 設定為 IFLAG \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="41638-131">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="41638-132">將此參數設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="41638-132">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="41638-133">值</span><span class="sxs-lookup"><span data-stu-id="41638-133">Value</span></span>                                                                                                                                                         | <span data-ttu-id="41638-134">意義</span><span class="sxs-lookup"><span data-stu-id="41638-134">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="41638-135"><dt>**IFLAG \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="41638-135"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="41638-136">框架中的資料發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="41638-136">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="41638-137"><dt>**IFLAG \_ 交換**</dt></span><span class="sxs-lookup"><span data-stu-id="41638-137"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="41638-138">在附加時， **文字** 位元組是非 Intel 格式。</span><span class="sxs-lookup"><span data-stu-id="41638-138">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="41638-139"><dt>**IFLAG \_ UNICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="41638-139"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="41638-140">在附加時間， **字串** 是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="41638-140">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41638-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="41638-141">Return value</span></span>

<span data-ttu-id="41638-142">如果函式成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="41638-142">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="41638-143">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="41638-143">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="41638-144">備註</span><span class="sxs-lookup"><span data-stu-id="41638-144">Remarks</span></span>

<span data-ttu-id="41638-145">**AttachPropertyInstanceEx** 函式會在 [**AttachProperties**](attachproperties.md)匯出函數的執行期間呼叫。</span><span class="sxs-lookup"><span data-stu-id="41638-145">The **AttachPropertyInstanceEx** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="41638-146">使用 AttachPropertyInstanceEx 將屬性附加至資料時，網路監視器會建立 [**PROPERTYINST**](propertyinst.md) 結構，以定義附加屬性的實例，以及定義擴充資料的 [**PROPERTYINSTEX**](propertyinstex.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="41638-146">When a property is attached to the data using AttachPropertyInstanceEx, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property and a [**PROPERTYINSTEX**](propertyinstex.md) structure that defines the extended data.</span></span>

<span data-ttu-id="41638-147">如果呼叫 **AttachPropertyInstanceEx** ，但未提供任何擴充資料， *LpDataEx* 參數為 **Null** 或 *LengthEx* 參數為0，則 **AttachPropertyInstanceEx** 呼叫的功能相當於 [**AttachPropertyInstance**](attachpropertyinstance.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="41638-147">If **AttachPropertyInstanceEx** is called and no extended data is provided, the *lpDataEx* parameter is **NULL** or the *LengthEx* parameter is 0, the **AttachPropertyInstanceEx** call is functionally equivalent to an [**AttachPropertyInstance**](attachpropertyinstance.md) call.</span></span>

<span data-ttu-id="41638-148">在 [**AttachProperties**](attachproperties.md)的執行期間，呼叫 [**AttachPropertyInstance**](attachpropertyinstance.md) 以使用存在於捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="41638-148">During the implementation of [**AttachProperties**](attachproperties.md), call [**AttachPropertyInstance**](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="41638-149">您也可以呼叫 **AttachPropertyInstanceEx** 函數來修改屬性資料。</span><span class="sxs-lookup"><span data-stu-id="41638-149">You can also call **AttachPropertyInstanceEx** function to modify the property data.</span></span> <span data-ttu-id="41638-150">不過，建議您使用存在於捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="41638-150">However, it is advised that you use the data as it exists in the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="41638-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="41638-151">Requirements</span></span>



| <span data-ttu-id="41638-152">需求</span><span class="sxs-lookup"><span data-stu-id="41638-152">Requirement</span></span> | <span data-ttu-id="41638-153">值</span><span class="sxs-lookup"><span data-stu-id="41638-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41638-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41638-154">Minimum supported client</span></span><br/> | <span data-ttu-id="41638-155">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41638-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="41638-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41638-156">Minimum supported server</span></span><br/> | <span data-ttu-id="41638-157">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41638-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="41638-158">標頭</span><span class="sxs-lookup"><span data-stu-id="41638-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="41638-159"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="41638-159"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="41638-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="41638-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="41638-161"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="41638-161"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="41638-162">DLL</span><span class="sxs-lookup"><span data-stu-id="41638-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41638-163"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41638-163"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




