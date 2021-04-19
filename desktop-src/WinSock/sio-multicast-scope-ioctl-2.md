---
description: 使用 SIO \_ 多播 \_ 領域命令程式碼來指定應進行多播的範圍。
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE Ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987708"
---
# <a name="sio_multicast_scope-ioctl"></a>SIO \_ 多播 \_ 範圍 Ioctl

當採用多播時，通常必須指定應進行多播的範圍。 這裡的範圍定義為要涵蓋的路由網路區段數目。 適用于 \_ WSPIoctl 的 SIO 多播 \_ 領域[](/previous-versions/windows/hardware/network/ff566296(v=vs.85))命令程式碼可用來控制此項。 範圍為零會指出多播傳輸不會放置在網路上，但是可以跨本機主機內的通訊端簡易性。 一個範圍值 (預設) 表示傳輸將放置在網路上，但不會跨越任何路由器。 範圍較高的值會決定可跨越的路由器數目。 請注意，這會對應至 IP 多播中的存留時間 (TTL) 參數。

 

 
