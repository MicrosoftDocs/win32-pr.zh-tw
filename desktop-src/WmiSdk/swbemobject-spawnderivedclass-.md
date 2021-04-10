---
description: 使用 \_ SWbemObject 物件的 SpawnDerivedClass 方法，從目前的物件建立衍生類別物件。 物件必須是類別定義，才能成為衍生物件的父類別。
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: 'SWbemObject.SpawnDerivedClass_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192064"
---
# <a name="swbemobjectspawnderivedclass_-method"></a><span data-ttu-id="5d2d6-104">SWbemObject. SpawnDerivedClass \_ 方法</span><span class="sxs-lookup"><span data-stu-id="5d2d6-104">SWbemObject.SpawnDerivedClass\_ method</span></span>

<span data-ttu-id="5d2d6-105">使用 [**SWbemObject**](swbemobject.md)物件的 **SpawnDerivedClass \_** 方法，從目前的物件建立衍生類別物件。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-105">Use the **SpawnDerivedClass\_** method of the [**SWbemObject**](swbemobject.md) object to create a derived class object from the current object.</span></span> <span data-ttu-id="5d2d6-106">物件必須是類別定義，才能成為衍生物件的父類別。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-106">The object must be a class definition that becomes the parent class of the spawned object.</span></span>

<span data-ttu-id="5d2d6-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2d6-108">語法</span><span class="sxs-lookup"><span data-stu-id="5d2d6-108">Syntax</span></span>


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5d2d6-109">參數</span><span class="sxs-lookup"><span data-stu-id="5d2d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2d6-110">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="5d2d6-110">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2d6-111">如果有指定，就會保留，且必須為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-111">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2d6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d2d6-112">Return value</span></span>

<span data-ttu-id="5d2d6-113">如果呼叫成功， [**SWbemObject**](swbemobject.md) 物件就會包含新的類別定義物件。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-113">If the call is successful, the [**SWbemObject**](swbemobject.md) object contains the new class definition object.</span></span> <span data-ttu-id="5d2d6-114">發生錯誤時，不會傳回任何物件。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-114">No object returns when there is an error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d2d6-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5d2d6-115">Error codes</span></span>

<span data-ttu-id="5d2d6-116">**SpawnDerivedClass \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-116">After the completion of the **SpawnDerivedClass\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5d2d6-117">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="5d2d6-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5d2d6-118">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5d2d6-119">**wbemErrIllegalOperation** -2147749918 (0x8004101E) </span><span class="sxs-lookup"><span data-stu-id="5d2d6-119">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="5d2d6-120">使用者要求了不合法的操作，例如從實例產生類別。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-120">User requested an illegal operation, such as spawning a class from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="5d2d6-121">**wbemErrIncompleteClass** -2147749920 (0x80041020) </span><span class="sxs-lookup"><span data-stu-id="5d2d6-121">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="5d2d6-122">來源類別未完整定義或向 WMI 註冊，因此不允許新的衍生類別。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-122">Source class was not completely defined or registered with WMI, so a new derived class is not permitted.</span></span>

</dd> <dt>

<span data-ttu-id="5d2d6-123">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="5d2d6-123">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5d2d6-124">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-124">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d2d6-125">備註</span><span class="sxs-lookup"><span data-stu-id="5d2d6-125">Remarks</span></span>

<span data-ttu-id="5d2d6-126">所傳回的物件會自動成為目前物件的子類別。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-126">The object that is returned automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="5d2d6-127">無法覆寫此行為。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-127">This behavior cannot be overridden.</span></span> <span data-ttu-id="5d2d6-128">沒有其他方法可讓您建立衍生類別。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-128">There is no other method by which you can create derived classes.</span></span>

<span data-ttu-id="5d2d6-129">您無法從您自己的用戶端進程的本機類別建立衍生類別。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-129">You cannot create a derived class from a class that is local to your own client process.</span></span> <span data-ttu-id="5d2d6-130">使用這個方法建立衍生類別之前，您必須先建立基類。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-130">Before use this method to create a derived class, you must create the base class.</span></span> <span data-ttu-id="5d2d6-131">若要建立基類，請呼叫 [**SWbemObject \_**](swbemobject-put-.md)，然後使用 [**SWbemServices 取得**](swbemservices-get.md)基類。</span><span class="sxs-lookup"><span data-stu-id="5d2d6-131">To create the base class, call [**SWbemObject.Put\_**](swbemobject-put-.md), and retrieve the base class using [**SWbemServices.Get**](swbemservices-get.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2d6-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d2d6-132">Requirements</span></span>



| <span data-ttu-id="5d2d6-133">需求</span><span class="sxs-lookup"><span data-stu-id="5d2d6-133">Requirement</span></span> | <span data-ttu-id="5d2d6-134">值</span><span class="sxs-lookup"><span data-stu-id="5d2d6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2d6-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d2d6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2d6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d2d6-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d2d6-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d2d6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2d6-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d2d6-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d2d6-139">標頭</span><span class="sxs-lookup"><span data-stu-id="5d2d6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d2d6-140"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2d6-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d2d6-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5d2d6-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="5d2d6-142"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5d2d6-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5d2d6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5d2d6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d2d6-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d2d6-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d2d6-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="5d2d6-145">CLSID</span></span><br/>                    | <span data-ttu-id="5d2d6-146">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="5d2d6-146">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="5d2d6-147">IID</span><span class="sxs-lookup"><span data-stu-id="5d2d6-147">IID</span></span><br/>                      | <span data-ttu-id="5d2d6-148">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="5d2d6-148">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




