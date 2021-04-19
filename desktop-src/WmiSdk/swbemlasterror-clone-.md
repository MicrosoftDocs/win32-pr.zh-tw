---
description: '\_SWbemLastError 物件的 clone 方法會傳回新的物件，這個物件是目前 SWbemLastError 物件的複製。'
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: 'SWbemLastError.Clone_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975172"
---
# <a name="swbemlasterrorclone_-method"></a><span data-ttu-id="2513f-103">SWbemLastError 複製 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="2513f-103">SWbemLastError.Clone\_ method</span></span>

<span data-ttu-id="2513f-104">[**SWbemLastError**](swbemlasterror.md)物件的 **clone \_** 方法會傳回新的物件，這個物件是目前 **SWbemLastError** 物件的複製。</span><span class="sxs-lookup"><span data-stu-id="2513f-104">The **Clone\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a new object that is a clone of the current **SWbemLastError** object.</span></span>

<span data-ttu-id="2513f-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2513f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2513f-106">語法</span><span class="sxs-lookup"><span data-stu-id="2513f-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="2513f-107">參數</span><span class="sxs-lookup"><span data-stu-id="2513f-107">Parameters</span></span>

<span data-ttu-id="2513f-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2513f-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2513f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2513f-109">Return value</span></span>

<span data-ttu-id="2513f-110">如果 **複製 \_** 方法成功，它會傳回新的 [**SWbemLastError**](swbemlasterror.md)物件。</span><span class="sxs-lookup"><span data-stu-id="2513f-110">If the **Clone\_** method is successful, it returns a new [**SWbemLastError**](swbemlasterror.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2513f-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2513f-111">Error codes</span></span>

<span data-ttu-id="2513f-112">**複製 \_** 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2513f-112">Upon the completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="2513f-113">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="2513f-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2513f-114">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2513f-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2513f-115">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="2513f-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2513f-116">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="2513f-116">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2513f-117">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="2513f-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2513f-118">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="2513f-118">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2513f-119">備註</span><span class="sxs-lookup"><span data-stu-id="2513f-119">Remarks</span></span>

<span data-ttu-id="2513f-120">使用複製方法來複製類別定義或實例。 **\_**</span><span class="sxs-lookup"><span data-stu-id="2513f-120">Use the **Clone\_** method to duplicate a class definition or instance.</span></span> <span data-ttu-id="2513f-121">當您需要在修改新的複本時，備份物件的原始複本時，這個方法很有用。</span><span class="sxs-lookup"><span data-stu-id="2513f-121">This method is useful when you need to back up the original copy of the object while you modify a new copy.</span></span> <span data-ttu-id="2513f-122">此外，也可以使用這個方法，從單一來源實例建立許多新的實例。</span><span class="sxs-lookup"><span data-stu-id="2513f-122">Also, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="2513f-123">例如，使用 [**SWbemObject SpawnInstance \_**](swbemobject-spawninstance-.md)來建立單一起始實例，並使用 **\_ SWbemLastError** 來快速產生實例的100複本。</span><span class="sxs-lookup"><span data-stu-id="2513f-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance and use **SWbemLastError.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="2513f-124">接著，您可以修改物件，並將特定的值提供給每個物件。</span><span class="sxs-lookup"><span data-stu-id="2513f-124">Subsequently, you can modify the objects, giving specific values to each object.</span></span>

<span data-ttu-id="2513f-125">您無法使用這個方法將類別定義轉換成實例，或是將實例轉換成類別定義。</span><span class="sxs-lookup"><span data-stu-id="2513f-125">It is not possible to use this method to convert a class definition to an instance or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="2513f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2513f-126">Requirements</span></span>



| <span data-ttu-id="2513f-127">需求</span><span class="sxs-lookup"><span data-stu-id="2513f-127">Requirement</span></span> | <span data-ttu-id="2513f-128">值</span><span class="sxs-lookup"><span data-stu-id="2513f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2513f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2513f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2513f-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2513f-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2513f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2513f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2513f-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2513f-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2513f-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2513f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2513f-134"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2513f-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2513f-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2513f-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="2513f-136"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2513f-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2513f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2513f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2513f-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2513f-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2513f-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="2513f-139">CLSID</span></span><br/>                    | <span data-ttu-id="2513f-140">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="2513f-140">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="2513f-141">IID</span><span class="sxs-lookup"><span data-stu-id="2513f-141">IID</span></span><br/>                      | <span data-ttu-id="2513f-142">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="2513f-142">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




