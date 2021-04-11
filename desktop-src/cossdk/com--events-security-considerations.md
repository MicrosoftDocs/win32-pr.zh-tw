---
description: 使用 COM + 事件服務時，您可以採取一些步驟，以確保事件中包含的任何機密資訊都不會受到危害。
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: COM + 事件安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936537"
---
# <a name="com-events-security-considerations"></a><span data-ttu-id="947a7-103">COM + 事件安全性考慮</span><span class="sxs-lookup"><span data-stu-id="947a7-103">COM+ Events Security Considerations</span></span>

<span data-ttu-id="947a7-104">使用 COM + 事件服務時，您可以採取一些步驟，以確保事件中包含的任何機密資訊都不會受到危害。</span><span class="sxs-lookup"><span data-stu-id="947a7-104">When using the COM+ events service, there are steps you can take to ensure that any sensitive information contained in an event is not compromised.</span></span>

<span data-ttu-id="947a7-105">事件發行者應該記住，任何可以寫入至 COM + 類別目錄的合作物件都可以訂閱您的事件。</span><span class="sxs-lookup"><span data-stu-id="947a7-105">Event publishers should keep in mind that any party that can write to your COM+ catalog can subscribe to your events.</span></span> <span data-ttu-id="947a7-106">因此，如果事件類別物件中包含的資訊是機密的，您應該使用 [元件服務管理] 工具來確認與訂閱者的通訊是否已針對包含事件類別元件的應用程式進行加密。</span><span class="sxs-lookup"><span data-stu-id="947a7-106">Therefore, if the information contained in an event class object is sensitive, you should use the Component Services administration tool to verify that communications with subscribers are encrypted for the application that contains the event class components.</span></span> <span data-ttu-id="947a7-107"> (在 [COM + 應用程式] 屬性工作表的 [ **安全性** ] 索引標籤上，選取 [封 **包隱私權** ] 作為 [ **呼叫的驗證等級** ] 設定 ) 。此外，您也應該使用 [事件篩選器](filtering-events-in-com-.md) ，協助確保只將事件傳遞給適當的訂閱者。</span><span class="sxs-lookup"><span data-stu-id="947a7-107">(On the **Security** tab of the COM+ application property sheet, select **Packet Privacy** as the **Authentication Level for Calls** setting.) Also, you should use [event filters](filtering-events-in-com-.md) to help ensure that events are delivered only to the appropriate subscribers.</span></span>

<span data-ttu-id="947a7-108">事件訂閱者必須記住，有權存取您的網路並知道事件類別物件的惡意物件，可能會建立錯誤的事件。</span><span class="sxs-lookup"><span data-stu-id="947a7-108">Event subscribers should keep in mind that a malicious party with access to your network and knowledge of your event class object could create false events.</span></span> <span data-ttu-id="947a7-109">因此，您應該使用以 [角色為基礎的安全性](role-based-security-administration.md) ，以協助確保事件類別物件之方法的呼叫端具有適當的認證，以執行您的執行所述的動作。</span><span class="sxs-lookup"><span data-stu-id="947a7-109">You should therefore use [role-based security](role-based-security-administration.md) to help ensure that callers of your event class object's methods have appropriate credentials to perform the actions described by your implementation.</span></span>

<span data-ttu-id="947a7-110">若要協助保護髮行者和訂閱者，請在受信任主機的私人網路中使用 COM + 事件服務，該服務是由防火牆與網際網路隔離。</span><span class="sxs-lookup"><span data-stu-id="947a7-110">To help protect both publishers and subscribers, use the COM+ Events service on a private network of trusted hosts that is isolated from the Internet by a firewall.</span></span>

## <a name="related-topics"></a><span data-ttu-id="947a7-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="947a7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="947a7-112">COM + 安全性</span><span class="sxs-lookup"><span data-stu-id="947a7-112">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="947a7-113">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="947a7-113">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="947a7-114">COM + 事件類別物件</span><span class="sxs-lookup"><span data-stu-id="947a7-114">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



