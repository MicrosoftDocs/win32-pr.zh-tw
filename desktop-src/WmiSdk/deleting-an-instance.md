---
description: 刪除實例是您可能會在 WMI 中執行的最常見刪除命令。
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: 刪除實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974617"
---
# <a name="deleting-an-instance"></a><span data-ttu-id="684b4-103">刪除實例</span><span class="sxs-lookup"><span data-stu-id="684b4-103">Deleting an Instance</span></span>

<span data-ttu-id="684b4-104">刪除實例是您可能會在 WMI 中執行的最常見刪除命令。</span><span class="sxs-lookup"><span data-stu-id="684b4-104">Deleting an instance is the most common delete command you are likely to perform in WMI.</span></span> <span data-ttu-id="684b4-105">就像刪除類別一樣，實際的命令相當簡單。</span><span class="sxs-lookup"><span data-stu-id="684b4-105">Like deleting a class, the actual command is fairly simple.</span></span> <span data-ttu-id="684b4-106">不過，根據您要刪除的實例類型而定，WMI 會有相當不同的執行方式。</span><span class="sxs-lookup"><span data-stu-id="684b4-106">However, WMI performs quite differently depending on the type of instance you are deleting.</span></span> <span data-ttu-id="684b4-107">如果實例是靜態的，WMI 就只會從 WMI 儲存機制中刪除實例。</span><span class="sxs-lookup"><span data-stu-id="684b4-107">If the instance is static, WMI simply deletes the instance from the WMI repository.</span></span> <span data-ttu-id="684b4-108">如需從 WMI 儲存機制移除類別和實例的詳細資訊，請參閱 [**pragma deleteclass**](pragma-deleteclass.md) 預處理器命令。</span><span class="sxs-lookup"><span data-stu-id="684b4-108">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="684b4-109">如果實例是動態的，WMI 必須在負責下列類別的提供者上呼叫 [**IWbemServices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) ：</span><span class="sxs-lookup"><span data-stu-id="684b4-109">If the instance is dynamic, WMI must call [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) on the providers that are responsible for the following classes:</span></span>

-   <span data-ttu-id="684b4-110">擁有實例的類別。</span><span class="sxs-lookup"><span data-stu-id="684b4-110">The class that owns the instance.</span></span>
-   <span data-ttu-id="684b4-111">擁有實例之類別的每個父類別。</span><span class="sxs-lookup"><span data-stu-id="684b4-111">Every parent class of the class that owns the instance.</span></span>
-   <span data-ttu-id="684b4-112">擁有實例之類別的每個子類別。</span><span class="sxs-lookup"><span data-stu-id="684b4-112">Every subclass of the class that owns the instance.</span></span>

<span data-ttu-id="684b4-113">刪除的成功與否取決於原始實例的最上層非抽象類別別。</span><span class="sxs-lookup"><span data-stu-id="684b4-113">The success of the deletion depends on the topmost nonabstract class for the original instance.</span></span> <span data-ttu-id="684b4-114">如果任何最上層非抽象類別別的提供者成功完成刪除，作業就會成功。</span><span class="sxs-lookup"><span data-stu-id="684b4-114">If the provider for any topmost nonabstract class succeeds in completing the deletion, the operation succeeds.</span></span> <span data-ttu-id="684b4-115">如需詳細資訊，請參閱 [**IWbemServices：:D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="684b4-115">For more information, see the Remarks section of [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span></span>

<span data-ttu-id="684b4-116">[適用于 WMI 的 COM API](com-api-for-wmi.md)有不同的方法可刪除實例和刪除物件。</span><span class="sxs-lookup"><span data-stu-id="684b4-116">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="684b4-117">下列程式說明如何使用 c + + 來刪除基類或衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="684b4-117">The following procedure describes how to use C++ to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="684b4-118">**使用 c + + 刪除基類或衍生類別的實例**</span><span class="sxs-lookup"><span data-stu-id="684b4-118">**To delete an instance of a base class or derived class using C++**</span></span>

-   <span data-ttu-id="684b4-119">請呼叫 [**iwbemservices：:D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) 或 [**Iwbemservices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="684b4-119">Call either the [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) methods.</span></span>

    <span data-ttu-id="684b4-120">顧名思義， [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) 會以非同步方式刪除實例，而 [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) 會以同步方式刪除實例。</span><span class="sxs-lookup"><span data-stu-id="684b4-120">As the name suggests, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) deletes an instance asynchronously while [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) deletes an instance synchronously.</span></span> <span data-ttu-id="684b4-121">若要使用 **DeleteInstanceAsync**，您也必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="684b4-121">To use **DeleteInstanceAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="684b4-122">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="684b4-122">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="684b4-123">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="684b4-123">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="684b4-124">[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)會使用相同的方法來刪除類別物件或實例。</span><span class="sxs-lookup"><span data-stu-id="684b4-124">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span>

<span data-ttu-id="684b4-125">下列程式描述如何使用 VBScript 來刪除基類或衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="684b4-125">The following procedure describes how to use VBScript to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="684b4-126">**使用 VBScript 刪除基類或衍生類別的實例**</span><span class="sxs-lookup"><span data-stu-id="684b4-126">**To delete an instance of a base class or derived class using VBScript**</span></span>

-   <span data-ttu-id="684b4-127">呼叫 [**SWbemObject. Delete \_**](swbemobject-delete-.md)或 [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md)方法。</span><span class="sxs-lookup"><span data-stu-id="684b4-127">Call either the [**SWbemObject.Delete\_**](swbemobject-delete-.md) or [**SWbemObject.DeleteAsync\_**](swbemobject-deleteasync-.md) methods.</span></span>

    <span data-ttu-id="684b4-128">顧名思義， [**Delete \_**](swbemobject-delete-.md)會在 [**DeleteAsync \_**](swbemobject-deleteasync-.md)以非同步方式刪除實例時，以同步方式刪除實例。</span><span class="sxs-lookup"><span data-stu-id="684b4-128">As the name suggests, [**Delete\_**](swbemobject-delete-.md) deletes an instance synchronously while [**DeleteAsync\_**](swbemobject-deleteasync-.md) deletes an instance asynchronously.</span></span> <span data-ttu-id="684b4-129">如需以非同步方式刪除實例的詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="684b4-129">For more information about deleting an instance asynchronously, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="684b4-130">下列範例說明如何使用 VBScript 刪除實例。</span><span class="sxs-lookup"><span data-stu-id="684b4-130">The following example describes how to delete an instance using VBScript.</span></span>

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> <span data-ttu-id="684b4-131">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="684b4-131">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="684b4-132">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="684b4-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



