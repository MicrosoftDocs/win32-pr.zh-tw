---
description: 您可能會發現，建立為一個父類別之子系的實例必須變更父類別，並成為不同父類別的子系。
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: 變更實例的繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849570"
---
# <a name="changing-the-inheritance-of-an-instance"></a><span data-ttu-id="af142-103">變更實例的繼承</span><span class="sxs-lookup"><span data-stu-id="af142-103">Changing the Inheritance of an Instance</span></span>

<span data-ttu-id="af142-104">您可能會發現，建立為一個父類別之子系的實例必須變更父類別，並成為不同父類別的子系。</span><span class="sxs-lookup"><span data-stu-id="af142-104">You may find a situation where an instance that was created as a child of one parent class must change parent classes and become the child of a different parent class.</span></span> <span data-ttu-id="af142-105">例如，您可能有衍生類別 **ManualService**、描述手動服務，以及描述自動服務的衍生類別 **AutoService**。</span><span class="sxs-lookup"><span data-stu-id="af142-105">For example, you may have a derived class, **ManualService**, describing a manual service, and a derived class, **AutoService**, describing an automatic service.</span></span> <span data-ttu-id="af142-106">這兩個類別都有許多屬性。</span><span class="sxs-lookup"><span data-stu-id="af142-106">Both classes have a large number of properties.</span></span> <span data-ttu-id="af142-107">並非所有屬性都相同。</span><span class="sxs-lookup"><span data-stu-id="af142-107">Not all properties are identical.</span></span> <span data-ttu-id="af142-108">若要將服務從手動變更為自動，您也必須將代表服務的實例從 **ManualService** 變更為 **AutoService**。</span><span class="sxs-lookup"><span data-stu-id="af142-108">To change a service from manual to automatic, you must also change the instance representing the service from **ManualService** to **AutoService**.</span></span> <span data-ttu-id="af142-109">在目前的 WMI 版本中，您無法呼叫 [**IWbemServices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 方法，並將 *PInst* 參數指向 **AutoService** 的實例，以及描述 **ManualService** 實例的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="af142-109">In the current version of WMI, you cannot call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) method with the *pInst* parameter pointing to an instance of **AutoService** and the key properties describing the **ManualService** instance.</span></span> <span data-ttu-id="af142-110">如果您這麼做，就會隱含地刪除原始的 **ManualService** 實例。</span><span class="sxs-lookup"><span data-stu-id="af142-110">If you do, you implicitly delete the original **ManualService** instance.</span></span> <span data-ttu-id="af142-111">基本上，在建立實例的類別之後，您只能藉由刪除實例並重新建立實例作為新父類別的實例，來變更實例的父類別。</span><span class="sxs-lookup"><span data-stu-id="af142-111">In essence, after you establish the class of an instance, you can only change the parent class of an instance by deleting the instance and recreating the instance as an instance of the new parent class.</span></span>

<span data-ttu-id="af142-112">下列程式描述如何將實例從某個類別移至另一個類別。</span><span class="sxs-lookup"><span data-stu-id="af142-112">The following procedure describes how to move an instance from one class to another class.</span></span>

<span data-ttu-id="af142-113">**將實例從一個類別移至另一個類別**</span><span class="sxs-lookup"><span data-stu-id="af142-113">**To move an instance from one class to another class**</span></span>

1.  <span data-ttu-id="af142-114">從原始類別中刪除實例。</span><span class="sxs-lookup"><span data-stu-id="af142-114">Delete the instance from the original class.</span></span>
2.  <span data-ttu-id="af142-115">在新類別下建立實例。</span><span class="sxs-lookup"><span data-stu-id="af142-115">Create the instance under the new class.</span></span>

    <span data-ttu-id="af142-116">WMI 不允許應用程式在新的類別中建立實例來移動實例，然後使用原始實例的金鑰來更新它。</span><span class="sxs-lookup"><span data-stu-id="af142-116">WMI does not allow applications to move an instance by creating it in the new class and then updating it with the key of the original instance.</span></span>

<span data-ttu-id="af142-117">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="af142-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



