---
title: RTMv2 程式設計問題
description: RTMv2 函式會使用下列假設來撰寫。
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- 程式設計問題，RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300800"
---
# <a name="rtmv2-programming-issues"></a><span data-ttu-id="1df62-104">RTMv2 程式設計問題</span><span class="sxs-lookup"><span data-stu-id="1df62-104">RTMv2 Programming Issues</span></span>

<span data-ttu-id="1df62-105">RTMv2 函式會使用下列假設來撰寫。</span><span class="sxs-lookup"><span data-stu-id="1df62-105">RTMv2 functions are written with the following assumptions.</span></span>

-   <span data-ttu-id="1df62-106">RTMv2 函數不會為用戶端配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="1df62-106">RTMv2 functions do not allocate memory for the client.</span></span> <span data-ttu-id="1df62-107">用戶端一律必須配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="1df62-107">The client must always allocate memory.</span></span>
-   <span data-ttu-id="1df62-108">當用戶端取消註冊時，它必須執行清除作業本身，例如釋出所有配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1df62-108">When a client is unregistering, it must perform clean-up operations itself, such as releasing all memory allocated.</span></span>
-   <span data-ttu-id="1df62-109">用戶端必須正確釋放控制碼;如果用戶端不會察覺到這種做法，可能會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="1df62-109">Clients must release handles correctly; memory leaks can occur if a client does not observe this practice.</span></span>

 

 




