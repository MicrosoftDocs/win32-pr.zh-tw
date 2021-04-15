---
description: 您可以使用 [元件服務] 系統管理工具，以程式設計的方式設定交易的超時，也可以使用 COM + 系統管理介面以程式設計的方式設定時間。
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: 設定交易 Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468477"
---
# <a name="setting-the-transaction-time-out"></a><span data-ttu-id="b6e71-103">設定交易 Time-Out</span><span class="sxs-lookup"><span data-stu-id="b6e71-103">Setting the Transaction Time-Out</span></span>

<span data-ttu-id="b6e71-104">您可以使用 [元件服務] 系統管理工具，以程式設計的方式設定交易的超時，也可以使用 [Com + 系統管理介面](com--administration-interfaces.md)以程式設計的方式設定時間。</span><span class="sxs-lookup"><span data-stu-id="b6e71-104">You can manually set the time-out for transactions by using the Component Services administrative tool, or you can programmatically configure the time-out by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span> <span data-ttu-id="b6e71-105">您可以在本機電腦層級以及個別元件上設定超時時間。</span><span class="sxs-lookup"><span data-stu-id="b6e71-105">The time-out can be configured at the local computer level and also for individual components.</span></span>

<span data-ttu-id="b6e71-106">**若要使用元件服務系統管理工具來設定本機電腦的交易超時**</span><span class="sxs-lookup"><span data-stu-id="b6e71-106">**To set the transaction time-out for the local computer by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="b6e71-107">在主控台樹中，以滑鼠 **按右鍵您** 要設定的本機電腦，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="b6e71-107">In the console tree, right-click the local computer you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="b6e71-108">在 [電腦屬性] 對話方塊中，按一下 [ **選項** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b6e71-108">In the computer properties dialog box, click the **Options** tab.</span></span>

3.  <span data-ttu-id="b6e71-109">在 [ **交易超時**] 下，輸入交易超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6e71-109">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="b6e71-110">預設的超時時間為60秒。</span><span class="sxs-lookup"><span data-stu-id="b6e71-110">The default time-out is 60 seconds.</span></span>

4.  <span data-ttu-id="b6e71-111">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="b6e71-111">Click **OK**.</span></span>

<span data-ttu-id="b6e71-112">**使用元件服務系統管理工具設定元件的交易超時**</span><span class="sxs-lookup"><span data-stu-id="b6e71-112">**To set the transaction time-out for a component by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="b6e71-113">在主控台樹中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="b6e71-113">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="b6e71-114">在 [元件屬性] 對話方塊中，按一下 [ **交易** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b6e71-114">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="b6e71-115">核取標示為 [覆 **寫全域交易超時值**] 的方塊。</span><span class="sxs-lookup"><span data-stu-id="b6e71-115">Check the box labeled **Override global transaction timeout value**.</span></span>

    > [!Note]  
    > <span data-ttu-id="b6e71-116">如果 **交易支援** 設定為 [ **已停用**]、[ **不支援**] 或 [ **受支援**]，您就無法選取方塊來覆寫全域交易超時值。</span><span class="sxs-lookup"><span data-stu-id="b6e71-116">You cannot check the box to override the global transaction time-out value if the **Transaction support** is set to **Disabled**, **Not Supported**, or **Supported**.</span></span>

     

4.  <span data-ttu-id="b6e71-117">在 [ **交易超時**] 下，輸入交易超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6e71-117">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="b6e71-118">預設的超時時間為0秒，這表示元件永遠不會造成交易超時。</span><span class="sxs-lookup"><span data-stu-id="b6e71-118">The default time-out is 0 seconds, which means that the component will never cause the transaction to time out.</span></span>

5.  <span data-ttu-id="b6e71-119">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="b6e71-119">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6e71-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b6e71-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6e71-121">管理 COM + 中的自動交易</span><span class="sxs-lookup"><span data-stu-id="b6e71-121">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



