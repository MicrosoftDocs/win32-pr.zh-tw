---
description: 內含物件的 Item 方法會從集合取得名為 Swbempropertyset。 這是這個物件的預設方法。
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: '內含專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195036"
---
# <a name="swbempropertysetitem-method"></a><span data-ttu-id="6690d-104">內含專案方法</span><span class="sxs-lookup"><span data-stu-id="6690d-104">SWbemPropertySet.Item method</span></span>

<span data-ttu-id="6690d-105">[**內含**](swbempropertyset.md)物件的 **Item** 方法會從集合取得名為 [**swbempropertyset**](swbemproperty.md) 。</span><span class="sxs-lookup"><span data-stu-id="6690d-105">The **Item** method of the [**SWbemPropertySet**](swbempropertyset.md) object gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="6690d-106">這是這個物件的預設方法。</span><span class="sxs-lookup"><span data-stu-id="6690d-106">This is the default method for this object.</span></span>

<span data-ttu-id="6690d-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="6690d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6690d-108">語法</span><span class="sxs-lookup"><span data-stu-id="6690d-108">Syntax</span></span>


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6690d-109">參數</span><span class="sxs-lookup"><span data-stu-id="6690d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6690d-110">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6690d-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6690d-111">必要。</span><span class="sxs-lookup"><span data-stu-id="6690d-111">Required.</span></span> <span data-ttu-id="6690d-112">要取得之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="6690d-112">Name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6690d-113">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6690d-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6690d-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="6690d-114">Reserved.</span></span> <span data-ttu-id="6690d-115">如果有指定，此值必須為零。</span><span class="sxs-lookup"><span data-stu-id="6690d-115">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6690d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6690d-116">Return value</span></span>

<span data-ttu-id="6690d-117">如果成功，則會傳回要求的 [**swbempropertyset**](swbemproperty.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6690d-117">If successful, the requested [**SWbemProperty**](swbemproperty.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6690d-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6690d-118">Error codes</span></span>

<span data-ttu-id="6690d-119">完成 **專案** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6690d-119">After the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6690d-120">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="6690d-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6690d-121">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="6690d-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="6690d-122">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="6690d-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6690d-123">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="6690d-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="6690d-124">**wbemErrOutOfMemory** -2147749896</span><span class="sxs-lookup"><span data-stu-id="6690d-124">**wbemErrOutOfMemory** - 2147749896</span></span>
</dt> <dd>

<span data-ttu-id="6690d-125">記憶體不足，無法執行此方法。</span><span class="sxs-lookup"><span data-stu-id="6690d-125">Not enough memory for this method to execute.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6690d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6690d-126">Requirements</span></span>



| <span data-ttu-id="6690d-127">需求</span><span class="sxs-lookup"><span data-stu-id="6690d-127">Requirement</span></span> | <span data-ttu-id="6690d-128">值</span><span class="sxs-lookup"><span data-stu-id="6690d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6690d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6690d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6690d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6690d-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6690d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6690d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6690d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6690d-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6690d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="6690d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6690d-134"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="6690d-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6690d-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6690d-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="6690d-136"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6690d-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6690d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6690d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6690d-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6690d-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6690d-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="6690d-139">CLSID</span></span><br/>                    | <span data-ttu-id="6690d-140">CLSID \_ 內含</span><span class="sxs-lookup"><span data-stu-id="6690d-140">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="6690d-141">IID</span><span class="sxs-lookup"><span data-stu-id="6690d-141">IID</span></span><br/>                      | <span data-ttu-id="6690d-142">IID \_ ISWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="6690d-142">IID\_ISWbemPropertySet</span></span><br/>                                                       |



 

 




