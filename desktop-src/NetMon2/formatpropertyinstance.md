---
description: 使用網路監視器提供的一般格式器來格式化屬性實例資料。
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: 'FormatPropertyInstance 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972597"
---
# <a name="formatpropertyinstance-function"></a><span data-ttu-id="1af70-103">FormatPropertyInstance 函式</span><span class="sxs-lookup"><span data-stu-id="1af70-103">FormatPropertyInstance function</span></span>

<span data-ttu-id="1af70-104">**FormatPropertyInstance** 函式會使用網路監視器提供的一般格式器來格式化屬性實例資料。</span><span class="sxs-lookup"><span data-stu-id="1af70-104">The **FormatPropertyInstance** function formats the property instance data using the generic formatter that Network Monitor provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af70-105">語法</span><span class="sxs-lookup"><span data-stu-id="1af70-105">Syntax</span></span>


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a><span data-ttu-id="1af70-106">參數</span><span class="sxs-lookup"><span data-stu-id="1af70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af70-107">*lpPropertyInst* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1af70-107">*lpPropertyInst* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1af70-108">包含實例資料之 [PROPERTYINST](propertyinst.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1af70-108">A pointer to a [PROPERTYINST](propertyinst.md) structure that contains the instance data.</span></span>

<span data-ttu-id="1af70-109">在輸入時，泛型格式器會採用其中一個 **PROPERTYINST** 聯集成員的實例資料，並將該資料轉換成預先定義的格式化字串。</span><span class="sxs-lookup"><span data-stu-id="1af70-109">On input, the generic formatter takes the instance data from one of the **PROPERTYINST** union members and converts that data to a predefined formatted string.</span></span>

<span data-ttu-id="1af70-110">在輸出中，一般格式器會將 **PROPERTYINST** 結構的 **szPropertyText** 成員設定為格式化字串的指標。</span><span class="sxs-lookup"><span data-stu-id="1af70-110">On output, the generic formatter sets the **szPropertyText** member of the **PROPERTYINST** structure to a pointer to the formatted string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af70-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1af70-111">Return value</span></span>

<span data-ttu-id="1af70-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="1af70-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1af70-113">如果函式不成功，則傳回值是 NMerr 中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1af70-113">If the function is unsuccessful, the return value is an error code from NMerr.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="1af70-114">備註</span><span class="sxs-lookup"><span data-stu-id="1af70-114">Remarks</span></span>

<span data-ttu-id="1af70-115">當需要一般格式器來格式化資料以在網路監視器 UI 的詳細資料窗格中顯示時，剖析器 DLL 會間接呼叫 **FormatPropertyInstance** 函數。</span><span class="sxs-lookup"><span data-stu-id="1af70-115">The parser DLL indirectly calls the **FormatPropertyInstance** function when the generic formatter is required to format data for display in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="1af70-116">當您定義屬性時，若要呼叫 **FormatPropertyInstance** ，請在 [PROPERTYINFO](propertyinfo.md)結構的 **InstanceData** 成員中指定它。</span><span class="sxs-lookup"><span data-stu-id="1af70-116">To call **FormatPropertyInstance** specify it in the **InstanceData** member of the [PROPERTYINFO](propertyinfo.md) structure when you define the property.</span></span>

> [!Note]  
> <span data-ttu-id="1af70-117">剖析器無法辨識當它必須格式化屬性的實例時，所呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="1af70-117">The parser does not recognize which function is called when it must format an instance of a property.</span></span> <span data-ttu-id="1af70-118">函式可以是 **FormatPropertyInstance** ，也可以是剖析器定義的自訂格式函數。</span><span class="sxs-lookup"><span data-stu-id="1af70-118">The function can be **FormatPropertyInstance** or a custom format function defined by the parser.</span></span> <span data-ttu-id="1af70-119">剖析器會呼叫屬性之 **PROPERTYINFO** 結構的 **InstanceData** 成員所指定的任何格式函數。</span><span class="sxs-lookup"><span data-stu-id="1af70-119">The parser calls whatever format function is specified by the **InstanceData** member of the **PROPERTYINFO** structure for the property.</span></span>

 

<span data-ttu-id="1af70-120">如需如何執行 [formatproperties](formatproperties.md)的詳細資訊和範例，請參閱 [執行 formatproperties](implementing-formatproperties.md)。</span><span class="sxs-lookup"><span data-stu-id="1af70-120">For more information and an example of how to implement [formatproperties](formatproperties.md), see [Implementing FormatProperties](implementing-formatproperties.md).</span></span> <span data-ttu-id="1af70-121">如需一般格式器如何格式化不同資料類型的詳細資訊，請參閱一般格式器 [輸出](generic-formatter-output.md)。</span><span class="sxs-lookup"><span data-stu-id="1af70-121">For more information about how the generic formatter formats different types of data, see [Generic Formatter Output](generic-formatter-output.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1af70-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1af70-122">Requirements</span></span>



| <span data-ttu-id="1af70-123">需求</span><span class="sxs-lookup"><span data-stu-id="1af70-123">Requirement</span></span> | <span data-ttu-id="1af70-124">值</span><span class="sxs-lookup"><span data-stu-id="1af70-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1af70-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1af70-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1af70-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1af70-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1af70-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1af70-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1af70-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1af70-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1af70-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1af70-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af70-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1af70-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1af70-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="1af70-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="1af70-132"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1af70-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1af70-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1af70-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1af70-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1af70-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af70-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1af70-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af70-136">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="1af70-136">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="1af70-137">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="1af70-137">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




