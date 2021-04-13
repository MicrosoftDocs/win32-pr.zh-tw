---
description: 除了類別和實例之外，WMI 還可讓您修改方法。 您會想要修改方法的主要原因是您變更了提供者中方法的執行方式。 如需詳細資訊，請參閱撰寫方法提供者。
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: 修改方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386059"
---
# <a name="modifying-a-method"></a><span data-ttu-id="eb56d-105">修改方法</span><span class="sxs-lookup"><span data-stu-id="eb56d-105">Modifying a Method</span></span>

<span data-ttu-id="eb56d-106">除了類別和實例之外，WMI 還可讓您修改方法。</span><span class="sxs-lookup"><span data-stu-id="eb56d-106">In addition to classes and instances, WMI allows you to modify a method.</span></span> <span data-ttu-id="eb56d-107">您會想要修改方法的主要原因是您變更了提供者中方法的執行方式。</span><span class="sxs-lookup"><span data-stu-id="eb56d-107">The main reason you would want to modify a method is if you changed the implementation of a method in a provider.</span></span> <span data-ttu-id="eb56d-108">如需詳細資訊，請參閱 [撰寫方法提供者](writing-a-method-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="eb56d-108">For more information, see [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="eb56d-109">修改方法不是可以在腳本中完成的作業。</span><span class="sxs-lookup"><span data-stu-id="eb56d-109">Modifying a method is not an operation that can be done in script.</span></span>

<span data-ttu-id="eb56d-110">下列程式描述如何以程式設計方式修改方法。</span><span class="sxs-lookup"><span data-stu-id="eb56d-110">The following procedure describes how to modify a method programmatically.</span></span>

<span data-ttu-id="eb56d-111">**以程式設計方式修改方法**</span><span class="sxs-lookup"><span data-stu-id="eb56d-111">**To modify a method programmatically**</span></span>

1.  <span data-ttu-id="eb56d-112">使用 [**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)的呼叫來取出類別定義。</span><span class="sxs-lookup"><span data-stu-id="eb56d-112">Retrieve the class definition with a call to [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

    <span data-ttu-id="eb56d-113">*PpInSignature* 和 *ppOutSignature* 這兩個 out 參數分別包含 in 參數類別和 out 參數類別。</span><span class="sxs-lookup"><span data-stu-id="eb56d-113">The two out parameters, *ppInSignature* and *ppOutSignature*, contain the in-parameter class and the out-parameter class, respectively.</span></span> <span data-ttu-id="eb56d-114">傳回值會以屬性的形式組合在 out 參數類別中，而且應該命名為 **ReturnValue**。</span><span class="sxs-lookup"><span data-stu-id="eb56d-114">The return value is bundled into the out-parameter class as a property, and should be named **ReturnValue**.</span></span>

2.  <span data-ttu-id="eb56d-115">使用對 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)、 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)內容或 [**IWbemClassObject：:D elete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)的呼叫來抓取和修改參數。</span><span class="sxs-lookup"><span data-stu-id="eb56d-115">Retrieve and modify the parameters with calls to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put), or [**IWbemClassObject::Delete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span></span>
3.  <span data-ttu-id="eb56d-116">呼叫 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)，將新版本的方法放回父類別。</span><span class="sxs-lookup"><span data-stu-id="eb56d-116">Place your new version of the method back into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="eb56d-117">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="eb56d-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



