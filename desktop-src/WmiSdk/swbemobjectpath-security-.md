---
description: SWbemObjectPath 物件的 Security 屬性是用來取得或設定物件路徑的安全性元件。
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: 'SWbemObjectPath.Security_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192061"
---
# <a name="swbemobjectpathsecurity_-property"></a><span data-ttu-id="ec7ed-103">SWbemObjectPath 安全性 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="ec7ed-103">SWbemObjectPath.Security\_ property</span></span>

<span data-ttu-id="ec7ed-104">[**SWbemObjectPath**](swbemobjectpath.md)物件的 **security** 屬性是用來取得或設定物件路徑的安全性元件。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-104">The **Security** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is used to get or set the security components of an object path.</span></span> <span data-ttu-id="ec7ed-105">請注意，它不會用來設定 **SWbemObjectPath** 物件本身的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-105">Note that it is not used to set security attributes of the **SWbemObjectPath** object itself.</span></span> <span data-ttu-id="ec7ed-106">它只能用來代表 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件的路徑安全性元件。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-106">It is used only to represent the security components of the path for an [**SWbemLocator**](swbemlocator.md) object.</span></span> <span data-ttu-id="ec7ed-107">這個屬性是 [**SWbemSecurity**](swbemsecurity.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-107">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="ec7ed-108">將 [**SWbemObjectPath**](swbemobjectset.md)物件的 [[**安全性 \_**](swbemobject-security-.md) ] 屬性設定為 **Null** ，會將無限存取權授與所有人。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-108">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectPath**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="ec7ed-109">如需詳細資訊，請參閱 [**SWbemSecurity**](swbemsecurity.md)。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="ec7ed-110">如需詳細資訊，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-110">For more information, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ec7ed-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ec7ed-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7ed-112">語法</span><span class="sxs-lookup"><span data-stu-id="ec7ed-112">Syntax</span></span>


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="ec7ed-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="ec7ed-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7ed-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec7ed-114">Requirements</span></span>



| <span data-ttu-id="ec7ed-115">需求</span><span class="sxs-lookup"><span data-stu-id="ec7ed-115">Requirement</span></span> | <span data-ttu-id="ec7ed-116">值</span><span class="sxs-lookup"><span data-stu-id="ec7ed-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7ed-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec7ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7ed-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec7ed-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec7ed-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec7ed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7ed-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec7ed-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec7ed-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ec7ed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec7ed-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ed-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec7ed-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ec7ed-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec7ed-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ed-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec7ed-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ec7ed-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7ed-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ed-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec7ed-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="ec7ed-127">CLSID</span></span><br/>                    | <span data-ttu-id="ec7ed-128">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="ec7ed-128">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="ec7ed-129">IID</span><span class="sxs-lookup"><span data-stu-id="ec7ed-129">IID</span></span><br/>                      | <span data-ttu-id="ec7ed-130">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="ec7ed-130">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="ec7ed-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec7ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7ed-132">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="ec7ed-132">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> <dt>

[<span data-ttu-id="ec7ed-133">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="ec7ed-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="ec7ed-134">設定用戶端 \_ 應用程式 \_ 處理安全性</span><span class="sxs-lookup"><span data-stu-id="ec7ed-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> </dl>

 

 




