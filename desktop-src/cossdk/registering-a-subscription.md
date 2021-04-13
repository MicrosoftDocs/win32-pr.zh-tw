---
description: 在 COM + 目錄中註冊事件類別之後，您可以將訂閱者加入至事件類別和訂閱者的訂閱。
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: 註冊訂用帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385982"
---
# <a name="registering-a-subscription"></a><span data-ttu-id="f9a4e-103">註冊訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="f9a4e-103">Registering a Subscription</span></span>

<span data-ttu-id="f9a4e-104">在 COM + 目錄中註冊事件類別之後，您可以將訂閱者加入至事件類別和訂閱者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-104">After you have registered an event class in the COM+ catalog, you can add subscribers to the event class and subscriptions to the subscribers.</span></span> <span data-ttu-id="f9a4e-105">訂閱可以訂閱單一方法或介面的所有方法。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-105">Subscriptions can subscribe to a single method or to all the methods of an interface.</span></span> <span data-ttu-id="f9a4e-106">若要接收對介面的多個方法（但不是每個方法）的呼叫，您必須為想要接收呼叫的每個方法加入訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-106">To receive calls on more than one method—but not to every method—of an interface, you must add a subscription for each method to which you want to receive a call.</span></span> <span data-ttu-id="f9a4e-107">元件服務管理工具可以搜尋 COM + 目錄中是否有已註冊的事件類別，這些類別支援訂閱者所執行的介面，並提供您訂閱的選擇。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-107">The Component Services administration tool can search the COM+ catalog for registered event classes that support the interfaces implemented by the subscriber and offers you the choice to subscribe.</span></span> <span data-ttu-id="f9a4e-108">選擇提供您所需事件的發行者。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-108">Choose the publisher that offers you the desired events.</span></span>

<span data-ttu-id="f9a4e-109">若要將訂閱者加入訂閱者元件，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f9a4e-109">To add subscribers to the subscriber component, use the following steps:</span></span>

1.  <span data-ttu-id="f9a4e-110">建立新的 COM + 應用程式並安裝訂閱者元件之後，以滑鼠右鍵按一下 [ **訂閱** ] 資料夾，以啟用 [Com + 新增訂閱]。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-110">After creating a new COM+ application and installing the subscriber component, right-click the **Subscriptions** folder to enable the COM+ New Subscription Wizard.</span></span>

2.  <span data-ttu-id="f9a4e-111">選擇您要從中接收事件的事件類別。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-111">Choose the event class from which you want to receive events.</span></span>

3.  <span data-ttu-id="f9a4e-112">輸入訂用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-112">Enter a name for the subscription.</span></span>

4.  <span data-ttu-id="f9a4e-113">啟用訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-113">Enable the subscription.</span></span>

5.  <span data-ttu-id="f9a4e-114">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-114">Click **OK**.</span></span>

<span data-ttu-id="f9a4e-115">當發行者應用程式想要引發事件時，發行者會將事件類別物件具現化，並在其上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-115">When a publisher application wants to fire an event, the publisher instantiates the event class object and calls a method on it.</span></span> <span data-ttu-id="f9a4e-116">COM + 會搜尋 COM + 類別目錄，以找出所有的訂閱者。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-116">COM+ searches the COM+ catalog to find all the subscribers.</span></span> <span data-ttu-id="f9a4e-117">它會建立訂閱者物件 (直接、排入佇列，或使用標記) ，然後在發行者最初進行的方法呼叫中傳遞。</span><span class="sxs-lookup"><span data-stu-id="f9a4e-117">It creates the subscriber object (directly, queued, or with a moniker) and passes on the method call originally made by the publisher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9a4e-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9a4e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9a4e-119">註冊事件類別</span><span class="sxs-lookup"><span data-stu-id="f9a4e-119">Registering an Event Class</span></span>](registering-an-event-class.md)
</dt> </dl>

 

 



