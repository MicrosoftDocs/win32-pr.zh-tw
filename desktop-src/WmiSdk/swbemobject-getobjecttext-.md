---
description: SWbemObject 物件的 GetObjectText 方法會傳回 \_ 物件的文字呈現。
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: 'SWbemObject.GetObjectText_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979064"
---
# <a name="swbemobjectgetobjecttext_-method"></a><span data-ttu-id="219e7-103">SWbemObject. GetObjectText \_ 方法</span><span class="sxs-lookup"><span data-stu-id="219e7-103">SWbemObject.GetObjectText\_ method</span></span>

<span data-ttu-id="219e7-104">[**SWbemObject**](swbemobject.md)物件的 **GetObjectText \_** 方法會傳回物件的文字呈現。</span><span class="sxs-lookup"><span data-stu-id="219e7-104">The **GetObjectText\_** method of the [**SWbemObject**](swbemobject.md) object returns a textual rendering of the object.</span></span> <span data-ttu-id="219e7-105">此物件可以用來顯示物件的內容。</span><span class="sxs-lookup"><span data-stu-id="219e7-105">This object can be used to display an object's contents.</span></span> <span data-ttu-id="219e7-106">目前，僅支援 MOF 語法作為輸出格式。</span><span class="sxs-lookup"><span data-stu-id="219e7-106">Currently, only the MOF syntax is supported as an output format.</span></span> <span data-ttu-id="219e7-107">請注意，傳回的 MOF 文字未包含物件的所有資訊;MOF 文字只包含足夠的資訊，讓 MOF 編譯器能夠重新建立原始物件。</span><span class="sxs-lookup"><span data-stu-id="219e7-107">Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="219e7-108">例如，沒有傳播的限定詞或父類別屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="219e7-108">For instance, there is no information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="219e7-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="219e7-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="219e7-110">語法</span><span class="sxs-lookup"><span data-stu-id="219e7-110">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="219e7-111">參數</span><span class="sxs-lookup"><span data-stu-id="219e7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="219e7-112">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="219e7-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="219e7-113">如果有指定，就會保留，且必須為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="219e7-113">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="219e7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="219e7-114">Return value</span></span>

<span data-ttu-id="219e7-115">如果成功，這個方法會傳回包含輸出文字的字串。</span><span class="sxs-lookup"><span data-stu-id="219e7-115">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="219e7-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="219e7-116">Error codes</span></span>

<span data-ttu-id="219e7-117">**GetObjectText \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="219e7-117">After the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="219e7-118">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="219e7-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="219e7-119">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="219e7-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="219e7-120">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="219e7-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="219e7-121">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="219e7-121">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="219e7-122">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="219e7-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="219e7-123">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="219e7-123">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="219e7-124">範例</span><span class="sxs-lookup"><span data-stu-id="219e7-124">Examples</span></span>

<span data-ttu-id="219e7-125">下列程式碼取自 TechNet 資源庫中 MOF 格式 VBScript 程式碼範例的 [Wmi 類別定義](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) ，並以 mof (受控物件格式) 語法，來取得和顯示 wmi 類別定義的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="219e7-125">The following code, taken from the [List the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript code sample in the TechNet Gallery, retrieves and displays the textual representation of a WMI class definition in MOF (Managed Object Format) syntax.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a><span data-ttu-id="219e7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="219e7-126">Requirements</span></span>



| <span data-ttu-id="219e7-127">需求</span><span class="sxs-lookup"><span data-stu-id="219e7-127">Requirement</span></span> | <span data-ttu-id="219e7-128">值</span><span class="sxs-lookup"><span data-stu-id="219e7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="219e7-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="219e7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="219e7-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="219e7-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="219e7-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="219e7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="219e7-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="219e7-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="219e7-133">標頭</span><span class="sxs-lookup"><span data-stu-id="219e7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="219e7-134"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="219e7-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="219e7-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="219e7-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="219e7-136"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="219e7-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="219e7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="219e7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="219e7-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="219e7-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="219e7-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="219e7-139">CLSID</span></span><br/>                    | <span data-ttu-id="219e7-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="219e7-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="219e7-141">IID</span><span class="sxs-lookup"><span data-stu-id="219e7-141">IID</span></span><br/>                      | <span data-ttu-id="219e7-142">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="219e7-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




