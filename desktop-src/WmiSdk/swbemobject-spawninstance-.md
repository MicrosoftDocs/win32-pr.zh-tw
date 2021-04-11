---
description: 使用 \_ SWbemObject 物件的 SpawnInstance 方法，建立類別的新實例。
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: 'SWbemObject.SpawnInstance_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195044"
---
# <a name="swbemobjectspawninstance_-method"></a><span data-ttu-id="35fbf-103">SWbemObject. SpawnInstance \_ 方法</span><span class="sxs-lookup"><span data-stu-id="35fbf-103">SWbemObject.SpawnInstance\_ method</span></span>

<span data-ttu-id="35fbf-104">使用 [**SWbemObject**](swbemobject.md)物件的 **SpawnInstance \_** 方法，建立類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="35fbf-104">Use the **SpawnInstance\_** method of the [**SWbemObject**](swbemobject.md) object to create a new instance of a class.</span></span> <span data-ttu-id="35fbf-105">目前的物件必須是透過 SWbemServices 取得的 WMI 所取得的類別定義，例如 [**Get**](swbemservices-get.md) 或 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)。</span><span class="sxs-lookup"><span data-stu-id="35fbf-105">The current object must be a class definition obtained from WMI via a method such as [**SWbemServices.Get**](swbemservices-get.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="35fbf-106">然後，使用此類別定義來建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="35fbf-106">Then, use this class definition to create new instances.</span></span> <span data-ttu-id="35fbf-107">在進程內的本機建立每個新的實例，然後呼叫 [**SWbemObject \_**](swbemobject-put-.md) ，以實際在 WMI 內建立實例。</span><span class="sxs-lookup"><span data-stu-id="35fbf-107">Create each new instance locally within the process, and then call [**SWbemObject.Put\_**](swbemobject-put-.md) to actually create the instance within WMI.</span></span>

> [!Note]  
> <span data-ttu-id="35fbf-108">支援從實例產生實例，但傳回的實例是空的。</span><span class="sxs-lookup"><span data-stu-id="35fbf-108">Spawning an instance from an instance is supported, but the returned instance is empty.</span></span>

 

<span data-ttu-id="35fbf-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="35fbf-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35fbf-110">語法</span><span class="sxs-lookup"><span data-stu-id="35fbf-110">Syntax</span></span>


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="35fbf-111">參數</span><span class="sxs-lookup"><span data-stu-id="35fbf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fbf-112">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="35fbf-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35fbf-113">如果已指定，則必須為零。</span><span class="sxs-lookup"><span data-stu-id="35fbf-113">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fbf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="35fbf-114">Return value</span></span>

<span data-ttu-id="35fbf-115">如果成功，此呼叫會傳回 [**SWbemObject**](swbemobject.md) 物件，其中包含類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="35fbf-115">If successful, this call returns an [**SWbemObject**](swbemobject.md) object that contains a new instance of the class.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35fbf-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="35fbf-116">Error codes</span></span>

<span data-ttu-id="35fbf-117">**SpawnInstance \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="35fbf-117">After the completion of the **SpawnInstance\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="35fbf-118">**wbemErrIncompleteClass** -2147749920 (0x80041020) </span><span class="sxs-lookup"><span data-stu-id="35fbf-118">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="35fbf-119">目前的物件不是有效的類別定義，而且無法產生新的實例。</span><span class="sxs-lookup"><span data-stu-id="35fbf-119">Current object is not a valid class definition, and it cannot spawn new instances.</span></span> <span data-ttu-id="35fbf-120">可能是未完成，或尚未使用 [**SWbemObject \_**](swbemobject-put-.md)向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="35fbf-120">Either it is incomplete, or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>

</dd> <dt>

<span data-ttu-id="35fbf-121">**wbemErrIllegalOperation** -2147749918 (0x8004101E) </span><span class="sxs-lookup"><span data-stu-id="35fbf-121">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="35fbf-122">如果在實例上使用這個方法，而不是在類別上，則傳回。</span><span class="sxs-lookup"><span data-stu-id="35fbf-122">Returned if this method is used on an instance instead of a class.</span></span>

</dd> <dt>

<span data-ttu-id="35fbf-123">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="35fbf-123">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="35fbf-124">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="35fbf-124">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="35fbf-125">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="35fbf-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="35fbf-126">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="35fbf-126">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35fbf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="35fbf-127">Requirements</span></span>



| <span data-ttu-id="35fbf-128">需求</span><span class="sxs-lookup"><span data-stu-id="35fbf-128">Requirement</span></span> | <span data-ttu-id="35fbf-129">值</span><span class="sxs-lookup"><span data-stu-id="35fbf-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35fbf-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35fbf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="35fbf-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35fbf-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35fbf-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35fbf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="35fbf-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35fbf-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35fbf-134">標頭</span><span class="sxs-lookup"><span data-stu-id="35fbf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fbf-135"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="35fbf-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35fbf-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="35fbf-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="35fbf-137"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35fbf-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35fbf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="35fbf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35fbf-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35fbf-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35fbf-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="35fbf-140">CLSID</span></span><br/>                    | <span data-ttu-id="35fbf-141">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="35fbf-141">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="35fbf-142">IID</span><span class="sxs-lookup"><span data-stu-id="35fbf-142">IID</span></span><br/>                      | <span data-ttu-id="35fbf-143">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="35fbf-143">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="35fbf-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35fbf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fbf-145">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="35fbf-145">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="35fbf-146">**SWbemObject。 Put\_**</span><span class="sxs-lookup"><span data-stu-id="35fbf-146">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="35fbf-147">**SWbemServices。 Get**</span><span class="sxs-lookup"><span data-stu-id="35fbf-147">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

 




