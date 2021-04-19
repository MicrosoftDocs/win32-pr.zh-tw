---
description: 建立命名空間的另一個方法是使用 WMI API，以程式設計方式建立命名空間。
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: 使用 WMI API 建立命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977847"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a><span data-ttu-id="97508-103">使用 WMI API 建立命名空間</span><span class="sxs-lookup"><span data-stu-id="97508-103">Creating a Namespace with the WMI API</span></span>

<span data-ttu-id="97508-104">建立命名空間的另一個方法是使用 WMI API，以程式設計方式建立命名空間。</span><span class="sxs-lookup"><span data-stu-id="97508-104">Another way of creating a namespace is to use the WMI API to create the namespace programmatically.</span></span> <span data-ttu-id="97508-105">以程式設計方式建立命名空間的優點是您可以從應用程式內建立命名空間。</span><span class="sxs-lookup"><span data-stu-id="97508-105">The advantage to creating a namespace programmatically is that you can create the namespace from within an application.</span></span> <span data-ttu-id="97508-106">不過，使用 WMI API 比使用受控物件格式 (MOF) 程式碼更複雜，而且您無法輕鬆地與其他開發人員共用您的命名空間。</span><span class="sxs-lookup"><span data-stu-id="97508-106">However, using the WMI API is more complex than using Managed Object Format (MOF) code, and you cannot as easily share your namespaces with other developers.</span></span>

<span data-ttu-id="97508-107">下列程式描述如何使用 WMI API 建立命名空間。</span><span class="sxs-lookup"><span data-stu-id="97508-107">The following procedure describes how to create a namespace using the WMI API.</span></span>

<span data-ttu-id="97508-108">**使用 WMI API 建立命名空間**</span><span class="sxs-lookup"><span data-stu-id="97508-108">**To create a namespace using the WMI API**</span></span>

1.  <span data-ttu-id="97508-109">使用 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)來抓取指向 [**\_ \_ 命名空間**](--namespace.md)系統類別之 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="97508-109">Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a pointer to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) object that points to the [**\_\_Namespace**](--namespace.md) system class.</span></span>
2.  <span data-ttu-id="97508-110">使用 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)的呼叫來定義 [**\_ \_ 命名空間**](--namespace.md)系統類別的實例。</span><span class="sxs-lookup"><span data-stu-id="97508-110">Define an instance of the [**\_\_Namespace**](--namespace.md) system class with a call to [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span></span>
3.  <span data-ttu-id="97508-111">使用 IWbemClassObject 的呼叫來設定 [**\_ \_ 命名空間**](--namespace.md)實例的 **Name** 屬性 [**：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)]。</span><span class="sxs-lookup"><span data-stu-id="97508-111">Set the **Name** property of the [**\_\_Namespace**](--namespace.md) instance with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>
4.  <span data-ttu-id="97508-112">使用對 [**IWbemServices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)的呼叫來建立命名空間。</span><span class="sxs-lookup"><span data-stu-id="97508-112">Create the namespace with a call to [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span></span>

    <span data-ttu-id="97508-113">[**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)的 *pInst* 參數應指向新的實例。</span><span class="sxs-lookup"><span data-stu-id="97508-113">The *pInst* parameter of [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) should point to the new instance.</span></span>

 

 



