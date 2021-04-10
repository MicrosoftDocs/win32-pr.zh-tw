---
description: 建立要接收連線通知的 DLL 之後，您必須向系統註冊。
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: 註冊以接收連接通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692923"
---
# <a name="registering-to-receive-connection-notifications"></a><span data-ttu-id="10804-103">註冊以接收連接通知</span><span class="sxs-lookup"><span data-stu-id="10804-103">Registering to Receive Connection Notifications</span></span>

<span data-ttu-id="10804-104">建立要接收連線通知的 DLL 之後，您必須向系統註冊。</span><span class="sxs-lookup"><span data-stu-id="10804-104">After you have created a DLL to receive connection notifications, you must register it with the system.</span></span> <span data-ttu-id="10804-105">若要這麼做，請在下列情況下新增 **REG \_ EXPAND \_ SZ** 值</span><span class="sxs-lookup"><span data-stu-id="10804-105">You do this by adding a **REG\_EXPAND\_SZ** value under the</span></span>

<span data-ttu-id="10804-106">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **NetworkProvider** \\ **Notifyees**</span><span class="sxs-lookup"><span data-stu-id="10804-106">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="10804-107">金鑰。</span><span class="sxs-lookup"><span data-stu-id="10804-107">key.</span></span> <span data-ttu-id="10804-108">這個值會指定執行 [連接通知 API](connection-notification-api.md)之 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="10804-108">This value specifies the path to the DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span>

<span data-ttu-id="10804-109">值可以有任何名稱。</span><span class="sxs-lookup"><span data-stu-id="10804-109">The value can have any name.</span></span> <span data-ttu-id="10804-110">**Notifyees** 索引鍵下的所有值都會被視為連接事件通知之 dll 的路徑。</span><span class="sxs-lookup"><span data-stu-id="10804-110">All values under the **Notifyees** key are treated as paths to DLLs that are notified of connection events.</span></span> <span data-ttu-id="10804-111">建議您使用可識別 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="10804-111">It is recommended that you use a name that identifies your DLL.</span></span> <span data-ttu-id="10804-112">這樣就能減少與其他連接通知應用程式發生名稱衝突的機率。</span><span class="sxs-lookup"><span data-stu-id="10804-112">This lessens the chance of a name conflict with other connection notification applications.</span></span>

<span data-ttu-id="10804-113">如需有關如何建立可接收連線通知的應用程式的詳細資訊，請參閱 [接收連接](receiving-connection-notifications.md)通知。</span><span class="sxs-lookup"><span data-stu-id="10804-113">For more information about how to create an application that receives connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md).</span></span>

 

 



