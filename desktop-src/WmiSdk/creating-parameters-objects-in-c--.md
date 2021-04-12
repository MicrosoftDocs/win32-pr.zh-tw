---
description: 如果執行的方法具有任何輸入引數，則 IWbemServices：： ExecMethod 或 ExecMethodAsync 方法需要 \_ \_ 參數系統類別做為 pInParams 中的容器。
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: 在 c + + 中建立參數物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192203"
---
# <a name="creating-parameters-objects-in-c"></a><span data-ttu-id="4f35e-103">在 c + + 中建立參數物件</span><span class="sxs-lookup"><span data-stu-id="4f35e-103">Creating Parameters Objects in C++</span></span>

<span data-ttu-id="4f35e-104">如果執行的方法具有任何輸入引數，則 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)或 [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)方法需要 [**\_ \_ 參數**](--parameters.md)系統類別做為 *pInParams* 中的容器。</span><span class="sxs-lookup"><span data-stu-id="4f35e-104">The [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) methods require the [**\_\_PARAMETERS**](--parameters.md) system class as a container in *pInParams* if the method they are executing has any input arguments.</span></span>

<span data-ttu-id="4f35e-105">下列程式描述如何建立 [**\_ \_ 參數**](--parameters.md)系統類別的實例來保存參數資訊。</span><span class="sxs-lookup"><span data-stu-id="4f35e-105">The following procedure describes how to create an instance of the [**\_\_PARAMETERS**](--parameters.md) system class to hold parameter information.</span></span>

<span data-ttu-id="4f35e-106">**若要建立參數的實例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f35e-106">**To create an instance of \_\_PARAMETERS**</span></span>

1.  <span data-ttu-id="4f35e-107">判斷包含方法定義之類別的類別路徑。</span><span class="sxs-lookup"><span data-stu-id="4f35e-107">Determine the class path for the class containing the method definition.</span></span>
2.  <span data-ttu-id="4f35e-108">使用從 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)傳入的類別路徑和 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)指標，呼叫 [**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)以取得輸入和輸出參數類別。</span><span class="sxs-lookup"><span data-stu-id="4f35e-108">Using the class path and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer passed in from [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), call [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve the input and output parameter classes.</span></span>

    <span data-ttu-id="4f35e-109">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)方法會傳回用來存取每個類別的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)指標。</span><span class="sxs-lookup"><span data-stu-id="4f35e-109">The [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for accessing each of these classes.</span></span>

3.  <span data-ttu-id="4f35e-110">使用輸出類別的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標，呼叫 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) 來建立類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4f35e-110">Using the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for the output class, call [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) to create an instance of the class.</span></span>
4.  <span data-ttu-id="4f35e-111">藉由設定對應至輸出值的屬性來填入類別實例，如果有方法的傳回值，則為 [ReturnValue](creating-a-method.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4f35e-111">Populate the class instance by setting the properties that correspond to the output values and, if there is a return value for the method, the [ReturnValue](creating-a-method.md) property.</span></span>
5.  <span data-ttu-id="4f35e-112">透過 [**IWbemObjectSink：：指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)方法，將 [**\_ \_ 參數**](--parameters.md)實例傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="4f35e-112">Pass the [**\_\_PARAMETERS**](--parameters.md) instance back to the caller through the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

<span data-ttu-id="4f35e-113">當方法提供者判斷輸入參數正確之後， *strMethodName* 所指向的方法可能仍會通過或失敗。</span><span class="sxs-lookup"><span data-stu-id="4f35e-113">After a method provider determines that the input parameters are correct, the method pointed to by *strMethodName* might still pass or fail.</span></span> <span data-ttu-id="4f35e-114">某些方法提供者會產生第二個執行緒來執行方法，讓方法的實際成功或失敗最後會透過 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)回報給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="4f35e-114">Some method providers spawn a second thread to implement the method so that the method's actual success or failure ends up being reported to the caller through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="4f35e-115">請注意， **IWbemObjectSink：： SetStatus** 不會收到提供者方法的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="4f35e-115">Note that **IWbemObjectSink::SetStatus** does not receive the return code of the provider method.</span></span> <span data-ttu-id="4f35e-116">但是，它會接收實際呼叫傳回機制的傳回碼，而且只適用于驗證呼叫是否發生，或是基於機械原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="4f35e-116">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f35e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f35e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f35e-118">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="4f35e-118">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="4f35e-119">**IWbemCallResult::GetResultObject**</span><span class="sxs-lookup"><span data-stu-id="4f35e-119">**IWbemCallResult::GetResultObject**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[<span data-ttu-id="4f35e-120">**IWbemServices：： ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="4f35e-120">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="4f35e-121">**IWbemServices：： ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="4f35e-121">**IWbemServices::ExecMethod**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



