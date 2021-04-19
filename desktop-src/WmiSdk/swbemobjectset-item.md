---
description: Swbemobjectset 搭配使用物件的 Item 方法會從集合取得 SWbemObject。
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975010"
---
# <a name="swbemobjectsetitem-method"></a><span data-ttu-id="2c9ca-103">Swbemobjectset 搭配使用專案方法</span><span class="sxs-lookup"><span data-stu-id="2c9ca-103">SWbemObjectSet.Item method</span></span>

<span data-ttu-id="2c9ca-104">[**Swbemobjectset 搭配使用**](swbemobjectset.md)物件的 **Item** 方法會從集合取得 [**SWbemObject**](swbemobject.md) 。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-104">The **Item** method of the [**SWbemObjectSet**](swbemobjectset.md) object gets an [**SWbemObject**](swbemobject.md) from the collection.</span></span>

<span data-ttu-id="2c9ca-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c9ca-106">語法</span><span class="sxs-lookup"><span data-stu-id="2c9ca-106">Syntax</span></span>


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a><span data-ttu-id="2c9ca-107">參數</span><span class="sxs-lookup"><span data-stu-id="2c9ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c9ca-108">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="2c9ca-108">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="2c9ca-109">必要。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-109">Required.</span></span> <span data-ttu-id="2c9ca-110">要從集合中取出之物件的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-110">Relative path of the object to retrieve from the collection.</span></span> <span data-ttu-id="2c9ca-111">範例： Win32 \_ LogicalDisk = "C："</span><span class="sxs-lookup"><span data-stu-id="2c9ca-111">Example: Win32\_LogicalDisk="C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c9ca-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c9ca-112">Return value</span></span>

<span data-ttu-id="2c9ca-113">如果成功，要求的 [**SWbemObject**](swbemobject.md) 物件就會傳回。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-113">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c9ca-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2c9ca-114">Error codes</span></span>

<span data-ttu-id="2c9ca-115">當 **專案** 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-115">Upon completion of the **Item** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="2c9ca-116">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="2c9ca-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2c9ca-117">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-117">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ca-118">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="2c9ca-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2c9ca-119">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-119">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ca-120">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="2c9ca-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2c9ca-121">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2c9ca-122">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="2c9ca-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="2c9ca-123">找不到要求的專案。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c9ca-124">備註</span><span class="sxs-lookup"><span data-stu-id="2c9ca-124">Remarks</span></span>

<span data-ttu-id="2c9ca-125">**Item** 方法可能需要很多的處理器時間，因為必須由集合的元素提供者完成列舉，才能傳回結果。</span><span class="sxs-lookup"><span data-stu-id="2c9ca-125">The **Item** method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c9ca-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c9ca-126">Requirements</span></span>



| <span data-ttu-id="2c9ca-127">需求</span><span class="sxs-lookup"><span data-stu-id="2c9ca-127">Requirement</span></span> | <span data-ttu-id="2c9ca-128">值</span><span class="sxs-lookup"><span data-stu-id="2c9ca-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9ca-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c9ca-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c9ca-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c9ca-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c9ca-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c9ca-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c9ca-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c9ca-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c9ca-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2c9ca-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c9ca-134"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c9ca-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c9ca-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2c9ca-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c9ca-136"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c9ca-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c9ca-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2c9ca-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c9ca-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c9ca-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c9ca-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="2c9ca-139">CLSID</span></span><br/>                    | <span data-ttu-id="2c9ca-140">CLSID \_ swbemobjectset 搭配使用</span><span class="sxs-lookup"><span data-stu-id="2c9ca-140">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="2c9ca-141">IID</span><span class="sxs-lookup"><span data-stu-id="2c9ca-141">IID</span></span><br/>                      | <span data-ttu-id="2c9ca-142">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c9ca-142">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




