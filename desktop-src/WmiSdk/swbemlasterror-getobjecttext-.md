---
description: SWbemLastError 物件的 GetObjectText 方法會傳回 \_ 受控物件格式 (MOF) 格式之物件的文字呈現。
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: 'SWbemLastError.GetObjectText_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944403"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a><span data-ttu-id="e5d2c-103">SWbemLastError. GetObjectText \_ 方法</span><span class="sxs-lookup"><span data-stu-id="e5d2c-103">SWbemLastError.GetObjectText\_ method</span></span>

<span data-ttu-id="e5d2c-104">[**SWbemLastError**](swbemlasterror.md)物件的 **GetObjectText \_** 方法會傳回 [受控物件格式 (MOF)](managed-object-format--mof-.md)格式之物件的文字呈現。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-104">The **GetObjectText\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a textual rendering of the object in a [Managed Object Format (MOF)](managed-object-format--mof-.md) format.</span></span> <span data-ttu-id="e5d2c-105">這個 MOF 物件可以用來顯示物件的內容。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-105">This MOF object can be used to display an object's contents.</span></span> <span data-ttu-id="e5d2c-106">請注意，傳回的 MOF 文字未包含物件的所有資訊，但只有足夠的資訊可供 MOF 編譯器重新建立原始物件。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-106">Notice that the MOF text that is returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="e5d2c-107">例如，您將找不到有關傳播的限定詞或父類別屬性的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-107">For instance, you will not find any information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="e5d2c-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d2c-109">語法</span><span class="sxs-lookup"><span data-stu-id="e5d2c-109">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e5d2c-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5d2c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d2c-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e5d2c-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d2c-112">這個參數是保留的，而且必須是 0 (零) 如果有指定的話）。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-112">This parameter is reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d2c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5d2c-113">Return value</span></span>

<span data-ttu-id="e5d2c-114">如果成功，這個方法會傳回包含輸出文字的字串。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-114">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5d2c-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e5d2c-115">Error codes</span></span>

<span data-ttu-id="e5d2c-116">**GetObjectText \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-116">Upon the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e5d2c-117">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="e5d2c-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e5d2c-118">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e5d2c-119">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="e5d2c-119">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e5d2c-120">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-120">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e5d2c-121">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="e5d2c-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e5d2c-122">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="e5d2c-122">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5d2c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5d2c-123">Requirements</span></span>



| <span data-ttu-id="e5d2c-124">需求</span><span class="sxs-lookup"><span data-stu-id="e5d2c-124">Requirement</span></span> | <span data-ttu-id="e5d2c-125">值</span><span class="sxs-lookup"><span data-stu-id="e5d2c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d2c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5d2c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d2c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5d2c-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5d2c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5d2c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d2c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5d2c-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5d2c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e5d2c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d2c-131"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d2c-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5d2c-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e5d2c-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5d2c-133"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e5d2c-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e5d2c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e5d2c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5d2c-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5d2c-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5d2c-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="e5d2c-136">CLSID</span></span><br/>                    | <span data-ttu-id="e5d2c-137">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="e5d2c-137">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="e5d2c-138">IID</span><span class="sxs-lookup"><span data-stu-id="e5d2c-138">IID</span></span><br/>                      | <span data-ttu-id="e5d2c-139">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="e5d2c-139">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




