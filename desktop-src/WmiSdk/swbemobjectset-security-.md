---
description: '\_Swbemobjectset 搭配使用物件的 security 屬性是用來取得或設定 swbemobjectset 搭配使用物件的安全性設定。 這個屬性是 SWbemSecurity 物件。'
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: 'SWbemObjectSet.Security_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984188"
---
# <a name="swbemobjectsetsecurity_-property"></a><span data-ttu-id="36cab-104">Swbemobjectset 搭配使用安全性 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="36cab-104">SWbemObjectSet.Security\_ property</span></span>

<span data-ttu-id="36cab-105">[**Swbemobjectset 搭配使用**](swbemobjectset.md)物件的 **security \_** 屬性是用來取得或設定 **swbemobjectset 搭配使用** 物件的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="36cab-105">The **Security\_** property of the [**SWbemObjectSet**](swbemobjectset.md) object is used to get or set the security settings for an **SWbemObjectSet** object.</span></span> <span data-ttu-id="36cab-106">這個屬性是 [**SWbemSecurity**](swbemsecurity.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="36cab-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="36cab-107">將 [**swbemobjectset 搭配使用**](swbemobjectset.md)物件的 [[**安全性 \_**](swbemobject-security-.md) ] 屬性設定為 **Null** ，會將無限存取權授與所有人。</span><span class="sxs-lookup"><span data-stu-id="36cab-107">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectSet**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="36cab-108">如需無限制存取含意的詳細資訊，請參閱 [**SWbemSecurity**](swbemsecurity.md)。</span><span class="sxs-lookup"><span data-stu-id="36cab-108">For more information about the implications of unlimited access, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="36cab-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="36cab-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="36cab-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="36cab-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36cab-111">語法</span><span class="sxs-lookup"><span data-stu-id="36cab-111">Syntax</span></span>


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="36cab-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="36cab-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="36cab-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="36cab-113">Requirements</span></span>



| <span data-ttu-id="36cab-114">需求</span><span class="sxs-lookup"><span data-stu-id="36cab-114">Requirement</span></span> | <span data-ttu-id="36cab-115">值</span><span class="sxs-lookup"><span data-stu-id="36cab-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36cab-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36cab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36cab-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36cab-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36cab-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36cab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36cab-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36cab-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36cab-120">標頭</span><span class="sxs-lookup"><span data-stu-id="36cab-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cab-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="36cab-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="36cab-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="36cab-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="36cab-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="36cab-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="36cab-124">DLL</span><span class="sxs-lookup"><span data-stu-id="36cab-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36cab-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36cab-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="36cab-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="36cab-126">CLSID</span></span><br/>                    | <span data-ttu-id="36cab-127">CLSID \_ swbemobjectset 搭配使用</span><span class="sxs-lookup"><span data-stu-id="36cab-127">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="36cab-128">IID</span><span class="sxs-lookup"><span data-stu-id="36cab-128">IID</span></span><br/>                      | <span data-ttu-id="36cab-129">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="36cab-129">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="36cab-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36cab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cab-131">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="36cab-131">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="36cab-132">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="36cab-132">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="36cab-133">保護腳本用戶端</span><span class="sxs-lookup"><span data-stu-id="36cab-133">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 




