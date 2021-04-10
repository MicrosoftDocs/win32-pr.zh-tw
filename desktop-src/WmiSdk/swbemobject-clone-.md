---
description: '\_SWbemObject 物件的 clone 方法會傳回新的物件，這個物件是目前物件的複本。'
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: 'SWbemObject.Clone_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027312"
---
# <a name="swbemobjectclone_-method"></a><span data-ttu-id="2f356-103">SWbemObject 複製 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="2f356-103">SWbemObject.Clone\_ method</span></span>

<span data-ttu-id="2f356-104">[**SWbemObject**](swbemobject.md)物件的 **clone \_** 方法會傳回新的物件，這個物件是目前物件的複本。</span><span class="sxs-lookup"><span data-stu-id="2f356-104">The **Clone\_** method of the [**SWbemObject**](swbemobject.md) object returns a new object that is a clone of the current object.</span></span>

<span data-ttu-id="2f356-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2f356-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f356-106">語法</span><span class="sxs-lookup"><span data-stu-id="2f356-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="2f356-107">參數</span><span class="sxs-lookup"><span data-stu-id="2f356-107">Parameters</span></span>

<span data-ttu-id="2f356-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2f356-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f356-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f356-109">Return value</span></span>

<span data-ttu-id="2f356-110">如果成功，這個方法會傳回新的 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2f356-110">If successful, this method returns a new [**SWbemObject**](swbemobject.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f356-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2f356-111">Error codes</span></span>

<span data-ttu-id="2f356-112">完成 **複製 \_** 方法之後， **Err** 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2f356-112">After completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="2f356-113">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="2f356-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2f356-114">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f356-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2f356-115">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="2f356-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2f356-116">未指定 **任何** 參數做為參數，因此在此使用方式中無法接受。</span><span class="sxs-lookup"><span data-stu-id="2f356-116">**Nothing** was specified as a parameter, and it is not acceptable in this usage.</span></span>

</dd> <dt>

<span data-ttu-id="2f356-117">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="2f356-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2f356-118">記憶體不足，無法複製物件。</span><span class="sxs-lookup"><span data-stu-id="2f356-118">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f356-119">備註</span><span class="sxs-lookup"><span data-stu-id="2f356-119">Remarks</span></span>

<span data-ttu-id="2f356-120">使用複製方法來複製類別定義或實例。 **\_**</span><span class="sxs-lookup"><span data-stu-id="2f356-120">Use the **Clone\_** method to duplicate a class definition or an instance.</span></span> <span data-ttu-id="2f356-121">當您在修改新複本時，需要物件的原始複本進行備份時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="2f356-121">This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy.</span></span> <span data-ttu-id="2f356-122">同樣地，您也可以使用這個方法，從單一來源實例建立許多新的實例。</span><span class="sxs-lookup"><span data-stu-id="2f356-122">Likewise, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="2f356-123">例如，您可以使用 [**SWbemObject SpawnInstance \_**](swbemobject-spawninstance-.md)來建立單一起始實例，並使用 **\_ SWbemObject** 來快速產生實例的100複本。</span><span class="sxs-lookup"><span data-stu-id="2f356-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance, and use **SWbemObject.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="2f356-124">接著，您可以修改物件，並提供每一個特定的值。</span><span class="sxs-lookup"><span data-stu-id="2f356-124">Subsequently, you can modify the objects, giving each one specific values.</span></span>

<span data-ttu-id="2f356-125">您無法使用這個方法將類別定義轉換成實例，或是將實例轉換成類別定義。</span><span class="sxs-lookup"><span data-stu-id="2f356-125">It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f356-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f356-126">Requirements</span></span>



| <span data-ttu-id="2f356-127">需求</span><span class="sxs-lookup"><span data-stu-id="2f356-127">Requirement</span></span> | <span data-ttu-id="2f356-128">值</span><span class="sxs-lookup"><span data-stu-id="2f356-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f356-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f356-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f356-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f356-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f356-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f356-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f356-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f356-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f356-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2f356-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f356-134"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f356-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f356-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2f356-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f356-136"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f356-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f356-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2f356-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f356-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f356-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f356-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="2f356-139">CLSID</span></span><br/>                    | <span data-ttu-id="2f356-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="2f356-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="2f356-141">IID</span><span class="sxs-lookup"><span data-stu-id="2f356-141">IID</span></span><br/>                      | <span data-ttu-id="2f356-142">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="2f356-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




