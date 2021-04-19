---
description: IPv6 路由器公告的內容會自動從路由表中已發佈的路由衍生。 Nonpublished 路由是用於路由傳送，但在建立路由器公告時則會忽略。
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: IPv6 路由器公告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992442"
---
# <a name="ipv6-router-advertisements"></a>IPv6 路由器公告

IPv6 路由器公告的內容會自動從路由表中已發佈的路由衍生。 Nonpublished 路由是用於路由傳送，但在建立路由器公告時則會忽略。

IPv6 的路由器公告一律包含來源連結層位址選項和 MTU 選項。 MTU 選項的值取自傳送介面的目前連結 MTU。 您可以使用 ipv6 ifc mtu 命令來變更這個值。

如果有已發佈的預設路由，則路由器通告只有非零的路由器存留期。 預設路由是零長度首碼的路由。

發佈的連結路由會導致路由器公告中的前置詞資訊選項。 如果連結前置詞有64位，首碼資訊選項會同時設定 L 和 bits，而接收它的主機將會 autoconfigure 位址。

傳送路由器公告的介面也會根據它所傳送的首碼資訊選項來 autoconfigure 自己的位址。

所有已發佈路由上的有限 nonaging 存留期 (例如，建議使用30分鐘) 。 如果您決定要撤銷路由，可以將路由變更為具有過時存留期。 路由將在數個路由器公告的過程中存留，然後從路由器和接收路由器通告的任何主機中消失。

主機透過路由器公告存留期找出的路由，且不會發佈。 從路由器公告的存留期，也能解決這種情況。

 

 



