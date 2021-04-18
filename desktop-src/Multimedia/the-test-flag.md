---
title: 測試旗標
description: 測試旗標
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST 旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311426"
---
# <a name="the-test-flag"></a><span data-ttu-id="f839a-104">測試旗標</span><span class="sxs-lookup"><span data-stu-id="f839a-104">The Test Flag</span></span>

<span data-ttu-id="f839a-105">「測試」 (MCI \_ 測試) 旗標會查詢裝置，以判斷它是否可以執行命令。</span><span class="sxs-lookup"><span data-stu-id="f839a-105">The "test" (MCI\_TEST) flag queries the device to determine if it can execute the command.</span></span> <span data-ttu-id="f839a-106">如果裝置無法執行命令，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f839a-106">The device returns an error if it cannot execute the command.</span></span> <span data-ttu-id="f839a-107">如果可以處理命令，則不會傳回任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="f839a-107">It returns no error if it can handle the command.</span></span> <span data-ttu-id="f839a-108">當您指定這個旗標時，MCI 會將控制權傳回給應用程式，而不會執行命令。</span><span class="sxs-lookup"><span data-stu-id="f839a-108">When you specify this flag, MCI returns control to the application without executing the command.</span></span>

<span data-ttu-id="f839a-109">所有命令都支援此旗標，但 [**open**](open.md) ([**MCI \_ 開啟**](mci-open.md)) 並 [**關閉**](close.md) ([**MCI \_ 關閉**](mci-close.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f839a-109">This flag is supported by digital-video and VCR devices for all commands except [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)).</span></span>

 

 




