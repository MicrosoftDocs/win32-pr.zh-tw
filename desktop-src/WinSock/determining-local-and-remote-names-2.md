---
description: WSPGetSockName 用來取得系結通訊端的本機位址。
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: 判斷本機和遠端名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026220"
---
# <a name="determining-local-and-remote-names"></a><span data-ttu-id="2bc7b-103">判斷本機和遠端名稱</span><span class="sxs-lookup"><span data-stu-id="2bc7b-103">Determining Local and Remote Names</span></span>

<span data-ttu-id="2bc7b-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) 用來取得系結通訊端的本機位址。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) is used to retrieve the local address for bound sockets.</span></span> <span data-ttu-id="2bc7b-105">在未先進行 [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))的情況下進行 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))呼叫時，這特別有用;**WSPGetSockName** 提供唯一的方法來判斷由提供者隱含設定的本機關聯。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-105">This is especially useful when a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) call has been made without doing a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) first; **WSPGetSockName** provides the only means to determine the local association which has been set implicitly by the provider.</span></span>

<span data-ttu-id="2bc7b-106">設定連接之後， [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) 可以用來判斷通訊端所連接之對等的位址。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-106">After a connection has been set up, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) can be used to determine the address of the peer to which a socket is connected.</span></span>

 

 
