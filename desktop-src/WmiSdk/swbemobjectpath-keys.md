---
description: SWbemObjectPath 物件的索引鍵屬性是 SWbemNamedValueSet 物件，其中包含索引鍵值系結。 這是唯讀的屬性。
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: 'SWbemObjectPath，索引鍵屬性 (Adoctint) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026489"
---
# <a name="swbemobjectpathkeys-property"></a><span data-ttu-id="b2818-104">SWbemObjectPath 索引鍵屬性</span><span class="sxs-lookup"><span data-stu-id="b2818-104">SWbemObjectPath.Keys property</span></span>

<span data-ttu-id="b2818-105">[**SWbemObjectPath**](swbemobjectpath.md)物件的索引 **鍵** 屬性是 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，其中包含索引鍵值系結。</span><span class="sxs-lookup"><span data-stu-id="b2818-105">The **Keys** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span> <span data-ttu-id="b2818-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="b2818-106">This property is read-only.</span></span>

<span data-ttu-id="b2818-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="b2818-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b2818-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b2818-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2818-109">語法</span><span class="sxs-lookup"><span data-stu-id="b2818-109">Syntax</span></span>


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a><span data-ttu-id="b2818-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="b2818-110">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2818-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b2818-111">Error codes</span></span>

<span data-ttu-id="b2818-112">在您取得索引 **鍵** 屬性之後， **Err** 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b2818-112">After you retrieve the **Keys** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="b2818-113">**wbemErrNotSupported** -2147749900 (0x8004100C) </span><span class="sxs-lookup"><span data-stu-id="b2818-113">**wbemErrNotSupported** - 2147749900 (0x8004100C)</span></span>
</dt> <dd>

<span data-ttu-id="b2818-114">功能或作業不支援。</span><span class="sxs-lookup"><span data-stu-id="b2818-114">The feature or operation is not supported.</span></span> <span data-ttu-id="b2818-115">如果腳本嘗試寫入這個屬性，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2818-115">This error is returned if a script attempts to write to this property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2818-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2818-116">Requirements</span></span>



| <span data-ttu-id="b2818-117">需求</span><span class="sxs-lookup"><span data-stu-id="b2818-117">Requirement</span></span> | <span data-ttu-id="b2818-118">值</span><span class="sxs-lookup"><span data-stu-id="b2818-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2818-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2818-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2818-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2818-120">Windows Vista</span></span><br/>                                                                                   |
| <span data-ttu-id="b2818-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2818-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2818-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2818-122">Windows Server 2008</span></span><br/>                                                                             |
| <span data-ttu-id="b2818-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b2818-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2818-124"><dt>Adoctint (包含 >wbemdisp.tlb) </dt></span><span class="sxs-lookup"><span data-stu-id="b2818-124"><dt>Adoctint.h (include Wbemdisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="b2818-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b2818-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2818-126"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2818-126"><dt>Wbemdisp.tlb</dt></span></span> </dl>                    |
| <span data-ttu-id="b2818-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b2818-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2818-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2818-128"><dt>Wbemdisp.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="b2818-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="b2818-129">CLSID</span></span><br/>                    | <span data-ttu-id="b2818-130">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="b2818-130">CLSID\_SWbemObjectPath</span></span><br/>                                                                          |
| <span data-ttu-id="b2818-131">IID</span><span class="sxs-lookup"><span data-stu-id="b2818-131">IID</span></span><br/>                      | <span data-ttu-id="b2818-132">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="b2818-132">IID\_ISWbemObjectPath</span></span><br/>                                                                           |



 

 




