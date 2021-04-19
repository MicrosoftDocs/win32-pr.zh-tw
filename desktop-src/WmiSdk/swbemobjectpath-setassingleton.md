---
description: SWbemObjectPath 物件的 SetAsSingleton 方法會強制路徑定址類別的單一 WMI 實例。 單一類別是一種永遠不能有多個實例的類別。
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: 'SWbemObjectPath. SetAsSingleton 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978395"
---
# <a name="swbemobjectpathsetassingleton-method"></a><span data-ttu-id="c1796-104">SWbemObjectPath. SetAsSingleton 方法</span><span class="sxs-lookup"><span data-stu-id="c1796-104">SWbemObjectPath.SetAsSingleton method</span></span>

<span data-ttu-id="c1796-105">[**SWbemObjectPath**](swbemobjectpath.md)物件的 **SetAsSingleton** 方法會強制路徑定址類別的單一 WMI 實例。</span><span class="sxs-lookup"><span data-stu-id="c1796-105">The **SetAsSingleton** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a singleton WMI instance of a class.</span></span> <span data-ttu-id="c1796-106">單一類別是一種永遠不能有多個實例的類別。</span><span class="sxs-lookup"><span data-stu-id="c1796-106">A singleton class is a class that can never have more than one instance.</span></span>

<span data-ttu-id="c1796-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c1796-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span> <span data-ttu-id="c1796-108">SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="c1796-108">SWbemObjectPath</span></span>

## <a name="syntax"></a><span data-ttu-id="c1796-109">語法</span><span class="sxs-lookup"><span data-stu-id="c1796-109">Syntax</span></span>


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a><span data-ttu-id="c1796-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1796-110">Parameters</span></span>

<span data-ttu-id="c1796-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c1796-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1796-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1796-112">Return value</span></span>

<span data-ttu-id="c1796-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c1796-113">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c1796-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c1796-114">Error codes</span></span>

<span data-ttu-id="c1796-115">**SetAsSingleton** 方法完成後， **Err** 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1796-115">Upon completion of the **SetAsSingleton** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="c1796-116">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="c1796-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c1796-117">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1796-117">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1796-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1796-118">Requirements</span></span>



| <span data-ttu-id="c1796-119">需求</span><span class="sxs-lookup"><span data-stu-id="c1796-119">Requirement</span></span> | <span data-ttu-id="c1796-120">值</span><span class="sxs-lookup"><span data-stu-id="c1796-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1796-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1796-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c1796-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1796-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1796-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1796-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c1796-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1796-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1796-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c1796-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1796-126"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1796-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1796-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c1796-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1796-128"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1796-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1796-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c1796-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1796-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1796-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1796-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="c1796-131">CLSID</span></span><br/>                    | <span data-ttu-id="c1796-132">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="c1796-132">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="c1796-133">IID</span><span class="sxs-lookup"><span data-stu-id="c1796-133">IID</span></span><br/>                      | <span data-ttu-id="c1796-134">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="c1796-134">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




