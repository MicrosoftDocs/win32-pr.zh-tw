---
description: 與刪除動態實例不同的是，刪除類別是一個簡單的程式。
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: 刪除類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985277"
---
# <a name="deleting-a-class"></a><span data-ttu-id="36b50-103">刪除類別</span><span class="sxs-lookup"><span data-stu-id="36b50-103">Deleting a Class</span></span>

<span data-ttu-id="36b50-104">與刪除動態實例不同的是，刪除類別是一個簡單的程式。</span><span class="sxs-lookup"><span data-stu-id="36b50-104">Unlike deleting a dynamic instance, deleting a class is a simple procedure.</span></span> <span data-ttu-id="36b50-105">不過，如先前所述，基本或衍生類別很少刪除。</span><span class="sxs-lookup"><span data-stu-id="36b50-105">However, as discussed earlier, base or derived classes are rarely deleted.</span></span> <span data-ttu-id="36b50-106">相反地，較常刪除實例。</span><span class="sxs-lookup"><span data-stu-id="36b50-106">Instead, an instance is more commonly deleted.</span></span> <span data-ttu-id="36b50-107">[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)會使用相同的方法來刪除類別物件或實例。</span><span class="sxs-lookup"><span data-stu-id="36b50-107">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span> <span data-ttu-id="36b50-108">如需詳細資訊，請參閱 [刪除實例](deleting-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="36b50-108">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span> <span data-ttu-id="36b50-109">如需從 WMI 儲存機制移除類別和實例的詳細資訊，請參閱 [**pragma deleteclass**](pragma-deleteclass.md) 預處理器命令。</span><span class="sxs-lookup"><span data-stu-id="36b50-109">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="36b50-110">[適用于 WMI 的 COM API](com-api-for-wmi.md)有不同的方法可刪除實例和刪除物件。</span><span class="sxs-lookup"><span data-stu-id="36b50-110">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="36b50-111">下列程式描述如何刪除基類或衍生類別。</span><span class="sxs-lookup"><span data-stu-id="36b50-111">The following procedure describes how to delete a base class or derived class.</span></span>

<span data-ttu-id="36b50-112">**刪除基類或衍生類別**</span><span class="sxs-lookup"><span data-stu-id="36b50-112">**To delete a base class or derived class**</span></span>

-   <span data-ttu-id="36b50-113">請呼叫 [**iwbemservices：:D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) 或 [**Iwbemservices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="36b50-113">Call either the [**IWbemServices::DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) or [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) method.</span></span>

    <span data-ttu-id="36b50-114">顧名思義， [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) 會在 [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) 同步刪除實例時，以非同步方式刪除實例。</span><span class="sxs-lookup"><span data-stu-id="36b50-114">As the name suggests, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) deletes an instance asynchronously while [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) deletes an instance synchronously.</span></span> <span data-ttu-id="36b50-115">若要使用 **DeleteClassAsync**，您也必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="36b50-115">To use **DeleteClassAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="36b50-116">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="36b50-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="36b50-117">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="36b50-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



