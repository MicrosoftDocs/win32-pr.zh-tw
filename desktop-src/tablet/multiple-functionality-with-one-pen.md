---
description: Tablet PC 畫筆可以有一個以上的一端可以與數位板互動。
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: 使用一個畫筆的多重功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320928"
---
# <a name="multiple-functionality-with-one-pen"></a><span data-ttu-id="726de-103">使用一個畫筆的多重功能</span><span class="sxs-lookup"><span data-stu-id="726de-103">Multiple Functionality with One Pen</span></span>

<span data-ttu-id="726de-104">Tablet PC 畫筆可以有一個以上的一端可以與數位板互動。</span><span class="sxs-lookup"><span data-stu-id="726de-104">A Tablet PC pen may have more than one end that can interact with the digitizer.</span></span> <span data-ttu-id="726de-105">如果畫筆的兩端都可以產生事件，則可以使用一端來配置筆墨、選取和點，而另一端也可以用於其他功能（例如清除）。</span><span class="sxs-lookup"><span data-stu-id="726de-105">If both ends of the pen can generate events, one end may be used to lay down ink, select, and point, and the other end may be used for other functions such as erasing.</span></span>

<span data-ttu-id="726de-106">若要執行這類功能，您的應用程式必須能夠判斷正在使用畫筆的哪一端，以及變更游標的外觀。</span><span class="sxs-lookup"><span data-stu-id="726de-106">To implement such functionality, your application must be able to determine which end of the pen is being used and hence when to change the appearance of the cursor.</span></span> <span data-ttu-id="726de-107">它可以藉由在資料 [**指標**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件上尋找 [**反向**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted)屬性的狀態來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="726de-107">It can do this by looking for the state of the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

<span data-ttu-id="726de-108">如需使用畫筆背面進行清除的特定詳細資訊，請參閱 [使用畫筆來清除筆墨](erasing-ink-with-the-pen.md)。</span><span class="sxs-lookup"><span data-stu-id="726de-108">For specific details about using the back of the pen for erasing, see [Erasing Ink with the Pen](erasing-ink-with-the-pen.md).</span></span> <span data-ttu-id="726de-109">此外， [筆跡清除範例](ink-erasing-sample.md) 會示範如何使用畫筆的背面來清除筆墨。</span><span class="sxs-lookup"><span data-stu-id="726de-109">In addition, the [Ink Erasing Sample](ink-erasing-sample.md) demonstrates how to use the back of the pen to erase ink.</span></span>

 

 



