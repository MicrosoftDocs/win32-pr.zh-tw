---
description: FormatProperties 匯出函式會格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。 如果您想要在 [詳細資料] 窗格中顯示資料，您必須在所有剖析器 Dll 中執行 FormatProperties export 函數。
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: 'FormatProperties 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972375"
---
# <a name="formatproperties-callback-function"></a><span data-ttu-id="8dc68-104">FormatProperties 回呼函式</span><span class="sxs-lookup"><span data-stu-id="8dc68-104">FormatProperties callback function</span></span>

<span data-ttu-id="8dc68-105">**FormatProperties** 匯出函式會格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="8dc68-105">The **FormatProperties** export function formats the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="8dc68-106">如果您想要在 [詳細資料] 窗格中顯示資料，您必須在所有剖析器 Dll 中執行 **FormatProperties** export 函數。</span><span class="sxs-lookup"><span data-stu-id="8dc68-106">If you want to display data in the details pane, you must implement the **FormatProperties** export function in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc68-107">語法</span><span class="sxs-lookup"><span data-stu-id="8dc68-107">Syntax</span></span>


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a><span data-ttu-id="8dc68-108">參數</span><span class="sxs-lookup"><span data-stu-id="8dc68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc68-109">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8dc68-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc68-110">要剖析之框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8dc68-110">Handle to the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="8dc68-111">*lpFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8dc68-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc68-112">框架第一個位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="8dc68-112">Pointer to the first byte of a frame.</span></span>

</dd> <dt>

<span data-ttu-id="8dc68-113">*lpProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8dc68-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc68-114">框架中通訊協定資料開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="8dc68-114">Pointer to the beginning of the protocol data in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="8dc68-115">*nPropertyInsts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8dc68-115">*nPropertyInsts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc68-116">*LpPropInst* 所提供的 [PROPERTYINST](propertyinst.md)結構數目。</span><span class="sxs-lookup"><span data-stu-id="8dc68-116">Number of [PROPERTYINST](propertyinst.md) structures provided by *lpPropInst*.</span></span>

</dd> <dt>

<span data-ttu-id="8dc68-117">*lpPropInst* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8dc68-117">*lpPropInst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc68-118">[PROPERTYINST](propertyinst.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="8dc68-118">Pointer to an array of [PROPERTYINST](propertyinst.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc68-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="8dc68-119">Return value</span></span>

<span data-ttu-id="8dc68-120">如果函式成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8dc68-120">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="8dc68-121">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8dc68-121">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dc68-122">備註</span><span class="sxs-lookup"><span data-stu-id="8dc68-122">Remarks</span></span>

<span data-ttu-id="8dc68-123">網路監視器會呼叫 **FormatProperties** 函式，以便在網路監視器 UI 的詳細資料窗格中顯示資料。</span><span class="sxs-lookup"><span data-stu-id="8dc68-123">Network Monitor calls the **FormatProperties** function to display data in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="8dc68-124">一般來說，會呼叫 **FormatProperties** 來格式化通訊協定的摘要行，然後格式化框架內的所有通訊協定屬性實例。</span><span class="sxs-lookup"><span data-stu-id="8dc68-124">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="8dc68-125">不過，網路監視器不保證它針對特定剖析器呼叫 **FormatProperties** 的次數。</span><span class="sxs-lookup"><span data-stu-id="8dc68-125">However, Network Monitor does not guarantee the number of times it calls **FormatProperties** for a specific parser.</span></span>

<span data-ttu-id="8dc68-126">在 **FormatProperties** 函式的執行期間，剖析器會間接呼叫 [FormatPropertyInstance](formatpropertyinstance.md) 函式，以使用網路監視器提供的一般格式器，或呼叫剖析器所定義的自訂格式器程式。</span><span class="sxs-lookup"><span data-stu-id="8dc68-126">During the implementation of the **FormatProperties** function, the parser indirectly calls the [FormatPropertyInstance](formatpropertyinstance.md) function to use the generic formatter that Network Monitor provides, or it can call a custom formatter procedure that is defined by the parser.</span></span> <span data-ttu-id="8dc68-127">您必須針對傳遞給 *lpPropInst* 參數中剖析器 DLL 的每個 [PROPERTYINST](propertyinst.md)結構，呼叫其中一個格式器。</span><span class="sxs-lookup"><span data-stu-id="8dc68-127">One of the formatters must be called for each [PROPERTYINST](propertyinst.md) structure passed to the parser DLL in the *lpPropInst* parameter.</span></span>



| <span data-ttu-id="8dc68-128">的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8dc68-128">For Information on</span></span>                                          | <span data-ttu-id="8dc68-129">請參閱</span><span class="sxs-lookup"><span data-stu-id="8dc68-129">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8dc68-130">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="8dc68-130">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="8dc68-131">解析 器</span><span class="sxs-lookup"><span data-stu-id="8dc68-131">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="8dc68-132">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="8dc68-132">Which entry points are included in the parser DLL.</span></span>          | [<span data-ttu-id="8dc68-133">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="8dc68-133">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="8dc68-134">如何執行 **FormatProperties**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="8dc68-134">How to implement **FormatProperties**  includes an example.</span></span> | [<span data-ttu-id="8dc68-135">執行 FormatProperties</span><span class="sxs-lookup"><span data-stu-id="8dc68-135">Implementing FormatProperties</span></span>](implementing-formatproperties.md) |
| <span data-ttu-id="8dc68-136">一般格式器如何格式化不同類型的資料。</span><span class="sxs-lookup"><span data-stu-id="8dc68-136">How the generic formatter formats different types of data.</span></span>  | [<span data-ttu-id="8dc68-137">一般格式器輸出</span><span class="sxs-lookup"><span data-stu-id="8dc68-137">Generic Formatter Output</span></span>](generic-formatter-output.md)           |



 

## <a name="requirements"></a><span data-ttu-id="8dc68-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dc68-138">Requirements</span></span>



| <span data-ttu-id="8dc68-139">需求</span><span class="sxs-lookup"><span data-stu-id="8dc68-139">Requirement</span></span> | <span data-ttu-id="8dc68-140">值</span><span class="sxs-lookup"><span data-stu-id="8dc68-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc68-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8dc68-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc68-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8dc68-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8dc68-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8dc68-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc68-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8dc68-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8dc68-145">標頭</span><span class="sxs-lookup"><span data-stu-id="8dc68-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc68-146"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8dc68-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc68-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dc68-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc68-148">FormatPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="8dc68-148">FormatPropertyInstance</span></span>](formatpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="8dc68-149">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="8dc68-149">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="8dc68-150">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="8dc68-150">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




