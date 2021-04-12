---
description: 參考共用通訊端的兩個 (或多個) 描述項，可能會與 i/o 相關時獨立使用。
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: 優先順序指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113021"
---
# <a name="precedence-guidelines"></a><span data-ttu-id="56975-103">優先順序指導方針</span><span class="sxs-lookup"><span data-stu-id="56975-103">Precedence Guidelines</span></span>

<span data-ttu-id="56975-104">參考共用通訊端的兩個 (或多個) 描述項，可能會與 i/o 相關時獨立使用。</span><span class="sxs-lookup"><span data-stu-id="56975-104">The two (or more) descriptors that reference a shared socket may be used independently as far as I/O is concerned.</span></span> <span data-ttu-id="56975-105">不過，Windows 通訊端介面並不會執行任何類型的存取控制，因此會負責協調共用通訊端上的作業所需的處理常式。</span><span class="sxs-lookup"><span data-stu-id="56975-105">However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket.</span></span> <span data-ttu-id="56975-106">共用通訊端的一般用途是有一個負責建立通訊端的進程，以及建立從通訊端到其他負責資訊交換的進程的連接。</span><span class="sxs-lookup"><span data-stu-id="56975-106">A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections hand off sockets to other processes that are responsible for information exchange.</span></span>

<span data-ttu-id="56975-107">在共用通訊端上支援多個未完成作業的一般指導方針，是建議服務提供者接受共用通訊端上的所有同時作業，特別是通訊端物件上的最新作業。</span><span class="sxs-lookup"><span data-stu-id="56975-107">The general guideline for supporting multiple outstanding operations on shared sockets is that a service provider is encouraged to honor all simultaneous operations on shared sockets, especially the most recent operation on a socket object.</span></span> <span data-ttu-id="56975-108">如果需要，這可能是因為取消一些先前但仍在等候的作業，而在此情況下會傳回 WSAEINTR。</span><span class="sxs-lookup"><span data-stu-id="56975-108">If need be, this may occur at the expense of canceling some of the previous but still pending operations, which will return WSAEINTR in this case.</span></span>

 

 



