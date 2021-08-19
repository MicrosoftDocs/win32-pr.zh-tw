---
description: 當採用多播時，通常必須指定應進行多播的範圍。
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: WSAIoctl 的 SIO_MULTICAST_SCOPE 命令程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38269167aa2ed142440b0e1105600d26c59514f72d749595ce44ecdf3a0998f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927367"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>\_ \_ 適用于 WSAIOCTL 的 SIO 多播領域命令程式碼

當採用多播時，通常必須指定應進行多播的 *範圍* 。 範圍定義為要涵蓋的路由網路區段數目。 範圍為零會指出多播傳輸不會放置在網路上，但是可以跨本機主機內的通訊端簡易性。 範圍值 1 (預設) 表示傳輸將放置在網路上，但不會跨越任何路由器。 範圍較高的值會決定可跨越的路由器數目。 請注意，這會對應至 IP 多播中的存留時間 (TTL) 參數。

函數 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 是用來將分葉節點聯結到 multipoint 會話中。 如需有關如何使用此函式的討論，請參閱下列內容。

 

 



