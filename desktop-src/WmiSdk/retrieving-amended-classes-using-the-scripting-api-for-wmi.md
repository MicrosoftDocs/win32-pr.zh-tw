---
description: 如果您使用適用于 WMI 的腳本 API 來取得或儲存當地語系化的類別資訊，請將地區設定指定為「標記」的一部分。
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: 使用適用于 WMI 的腳本 API 來抓取修改過的類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983554"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a><span data-ttu-id="7b421-103">使用適用于 WMI 的腳本 API 來抓取修改過的類別</span><span class="sxs-lookup"><span data-stu-id="7b421-103">Retrieving Amended Classes Using the Scripting API for WMI</span></span>

<span data-ttu-id="7b421-104">如果您使用適用于 WMI 的腳本 API 來取得或儲存當地語系化的類別資訊，請將地區設定指定為「標記」的一部分。</span><span class="sxs-lookup"><span data-stu-id="7b421-104">If you are using the Scripting API for WMI to retrieve or store localized class information, specify the locale as part of a moniker.</span></span> <span data-ttu-id="7b421-105">或者，您可以在 *strLocale* 參數中提供 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 方法的地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="7b421-105">Or, you can supply the locale name in the *strLocale* parameter to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span> <span data-ttu-id="7b421-106">讀取或寫入修改過的類別時，表示您想要使用當地語系化的類別定義，方法是指定 [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) 做為您所呼叫之方法的 *iFlags* 參數旗標。</span><span class="sxs-lookup"><span data-stu-id="7b421-106">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) as a flag for the *iFlags* parameter of the method you call.</span></span> <span data-ttu-id="7b421-107">針對 PowerShell，您可以在 [>get-wmiobject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true)上使用 *-locale* 參數來指定地區設定。</span><span class="sxs-lookup"><span data-stu-id="7b421-107">For PowerShell, you can use the *-locale* parameter on [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) to specify the locale.</span></span>

<span data-ttu-id="7b421-108">下列程式碼範例示範如何使用 WMI 腳本的標記或-locale 參數來取得當地語系化的類別。</span><span class="sxs-lookup"><span data-stu-id="7b421-108">The following code example shows how to retrieve a localized class by using a WMI scripting moniker or the -locale parameter.</span></span>


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





<span data-ttu-id="7b421-109">下列程式碼範例示範如何設定 locale 參數，並使用 [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) 旗標。</span><span class="sxs-lookup"><span data-stu-id="7b421-109">The following code example shows how to set the locale parameter and use the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> <span data-ttu-id="7b421-110">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="7b421-110">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="7b421-111">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="7b421-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="7b421-112">下表列出接受 [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) 旗標的方法。</span><span class="sxs-lookup"><span data-stu-id="7b421-112">The following table lists the methods that accept the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>



| <span data-ttu-id="7b421-113">同步方法</span><span class="sxs-lookup"><span data-stu-id="7b421-113">Synchronous Method</span></span>                                                 | <span data-ttu-id="7b421-114">非同步方法</span><span class="sxs-lookup"><span data-stu-id="7b421-114">Asynchronous Method</span></span>                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="7b421-115">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="7b421-115">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)   | [<span data-ttu-id="7b421-116">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="7b421-116">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)   |
| [<span data-ttu-id="7b421-117">**SWbemObject 子類別\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-117">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)        | [<span data-ttu-id="7b421-118">**SWbemObject. SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-118">**SWbemObject.SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)        |
| [<span data-ttu-id="7b421-119">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="7b421-119">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)     | [<span data-ttu-id="7b421-120">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="7b421-120">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)     |
| [<span data-ttu-id="7b421-121">**SWbemObject 實例\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-121">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)          | [<span data-ttu-id="7b421-122">**SWbemObject. InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-122">**SWbemObject.InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)          |
| [<span data-ttu-id="7b421-123">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="7b421-123">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)         | [<span data-ttu-id="7b421-124">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="7b421-124">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)         |
| [<span data-ttu-id="7b421-125">**SWbemServices。 Get**</span><span class="sxs-lookup"><span data-stu-id="7b421-125">**SWbemServices.Get**</span></span>](swbemservices-get.md)                     | [<span data-ttu-id="7b421-126">**SWbemServices. GetAsync**</span><span class="sxs-lookup"><span data-stu-id="7b421-126">**SWbemServices.GetAsync**</span></span>](swbemservices-getasync.md)                     |
| [<span data-ttu-id="7b421-127">**SWbemObject。 Put\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-127">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)                      | [<span data-ttu-id="7b421-128">**SWbemObject. PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-128">**SWbemObject.PutAsync\_**</span></span>](swbemobject-putasync-.md)                      |
| [<span data-ttu-id="7b421-129">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="7b421-129">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)   | [<span data-ttu-id="7b421-130">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="7b421-130">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)   |
| [<span data-ttu-id="7b421-131">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-131">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)        | [<span data-ttu-id="7b421-132">**SWbemObject. ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-132">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)        |
| [<span data-ttu-id="7b421-133">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="7b421-133">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md) | [<span data-ttu-id="7b421-134">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="7b421-134">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md) |
| [<span data-ttu-id="7b421-135">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-135">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)      | [<span data-ttu-id="7b421-136">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="7b421-136">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)      |



 

 

 
