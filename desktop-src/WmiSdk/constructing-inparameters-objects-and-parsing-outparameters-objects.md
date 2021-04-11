---
description: 一般情況下，直接存取相當適合用來呼叫 WMI 提供者方法。
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: 建立 InParameters 物件和剖析 OutParameters 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944717"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a><span data-ttu-id="ee7f1-103">建立 InParameters 物件和剖析 OutParameters 物件</span><span class="sxs-lookup"><span data-stu-id="ee7f1-103">Constructing InParameters Objects and Parsing OutParameters Objects</span></span>

<span data-ttu-id="ee7f1-104">一般情況下，直接存取相當適合用來呼叫 WMI [*提供者方法*](gloss-p.md)。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-104">Normally, direct access is adequate to call a WMI [*provider method*](gloss-p.md).</span></span> <span data-ttu-id="ee7f1-105">直接存取表示使用 *物件方法* 語法來執行方法。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-105">Direct access means executing a method by using *object.method* syntax.</span></span> <span data-ttu-id="ee7f1-106">不過，在某些情況下，無法使用直接存取。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-106">However, in some cases, direct access cannot be used.</span></span> <span data-ttu-id="ee7f1-107">此外，從腳本以非同步方式呼叫提供者方法需要 [**ExecMethodAsync**](swbemobject-execmethodasync-.md) 的呼叫類型。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-107">Also, calling a provider method asynchronously from a script requires an [**ExecMethodAsync**](swbemobject-execmethodasync-.md) type of call.</span></span>

> [!Note]  
> <span data-ttu-id="ee7f1-108">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-108">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="ee7f1-109">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="ee7f1-110">方法輸入和輸出參數的順序定義于方法的受控物件格式 (MOF) 架構中。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-110">The order of method input and output parameters is defined in the Managed Object Format (MOF) schema for the method.</span></span> <span data-ttu-id="ee7f1-111">當 [mofcomp.exe](mofcomp.md)重新編譯類別時，WMI 無法防止參數順序變更。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-111">WMI does not prevent the parameter order from being changed when the class is recompiled by [mofcomp](mofcomp.md).</span></span> <span data-ttu-id="ee7f1-112">藉由使用 [**InParameters**](swbemmethod-inparameters.md) 物件，您可以避免因為輸入參數是依名稱識別而變更的架構所產生的問題。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-112">By using an [**InParameters**](swbemmethod-inparameters.md) object, you can avoid problems that result from changed schema because the input parameters are identified by name.</span></span> <span data-ttu-id="ee7f1-113">藉由檢查每個輸入參數的 **識別碼** 辨識符號，可以看到正確的參數。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-113">The correct parameter can be seen by examining the **ID** qualifier of each input parameter.</span></span> <span data-ttu-id="ee7f1-114">第一個參數的 **識別碼** 值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-114">The first parameter has an **ID** value of 0 (zero).</span></span>

<span data-ttu-id="ee7f1-115">在無法直接執行方法的情況下， [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md)、 [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md)、 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)和 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)方法會提供另一種方法來執行提供者方法。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-115">[**The SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods provide an alternate way to execute a provider method in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="ee7f1-116">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="ee7f1-117">如需參數的詳細資訊，請參閱 [建立 InParameters 物件](constructing-inparameters-objects.md) 和 [剖析 OutParameters 物件](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="ee7f1-117">For more information about parameters, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

 

 



