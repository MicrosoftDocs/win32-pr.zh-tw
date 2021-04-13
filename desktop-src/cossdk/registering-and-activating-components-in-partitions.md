---
description: 在分割區中註冊和啟用元件
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: 在分割區中註冊和啟用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510544"
---
# <a name="registering-and-activating-components-in-partitions"></a><span data-ttu-id="020be-103">在分割區中註冊和啟用元件</span><span class="sxs-lookup"><span data-stu-id="020be-103">Registering and Activating Components in Partitions</span></span>

<span data-ttu-id="020be-104">建立分割區之後，下一個步驟是在該分割區內註冊您的 COM + 元件。</span><span class="sxs-lookup"><span data-stu-id="020be-104">After a partition has been created, the next step is register your COM+ components within that partition.</span></span> <span data-ttu-id="020be-105">當建立新的 COM + 應用程式，或將現有的 COM + 應用程式安裝到磁碟分割時，就會在分割區內註冊元件。</span><span class="sxs-lookup"><span data-stu-id="020be-105">A component is registered within a partition when a new COM+ application is created or when an existing COM+ application is installed into the partition.</span></span> <span data-ttu-id="020be-106">為了在多個資料分割包含相同的 COM + 元件時簡化註冊管理，分割區服務可讓系統管理員將應用程式或元件從某個分割區複製到另一個分割區。</span><span class="sxs-lookup"><span data-stu-id="020be-106">To ease the administration of registration when multiple partitions contain the same COM+ components, the partitions service allows an administrator to copy applications or components from one partition into another.</span></span> <span data-ttu-id="020be-107">當系統複製 COM + 應用程式或元件時，除了應用程式的身分識別或角色的任何成員以外，所有相關聯的資料分割屬性都會連同該屬性一起複製。</span><span class="sxs-lookup"><span data-stu-id="020be-107">When a COM+ application or a component is copied, all associated partition properties are copied with it, except the application's identity or any of the members of a role.</span></span>

<span data-ttu-id="020be-108">當用戶端程式呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) 函式來具現化物件時，com + 會執行兩個不同的步驟，如下所示：</span><span class="sxs-lookup"><span data-stu-id="020be-108">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function to instantiate an object, COM+ performs two distinct steps, as follows:</span></span>

1.  <span data-ttu-id="020be-109">尋找元件所在的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="020be-109">Locates the partition in which the component resides</span></span>
2.  <span data-ttu-id="020be-110">在該分割區內找出正確的元件</span><span class="sxs-lookup"><span data-stu-id="020be-110">Locates the correct component within that partition</span></span>

<span data-ttu-id="020be-111">本節中的下列主題將詳細說明這些步驟：</span><span class="sxs-lookup"><span data-stu-id="020be-111">The following topics in this section describe these steps in detail:</span></span>

-   [<span data-ttu-id="020be-112">在啟用期間尋找磁碟分割</span><span class="sxs-lookup"><span data-stu-id="020be-112">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
-   [<span data-ttu-id="020be-113">找出要啟用的元件</span><span class="sxs-lookup"><span data-stu-id="020be-113">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)

## <a name="related-topics"></a><span data-ttu-id="020be-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="020be-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="020be-115">應用程式設計限制</span><span class="sxs-lookup"><span data-stu-id="020be-115">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="020be-116">COM + 佇列元件和分割區</span><span class="sxs-lookup"><span data-stu-id="020be-116">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="020be-117">分割區執行</span><span class="sxs-lookup"><span data-stu-id="020be-117">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="020be-118">什麼是 COM + 磁碟分割？</span><span class="sxs-lookup"><span data-stu-id="020be-118">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 
