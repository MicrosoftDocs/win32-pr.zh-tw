---
title: 靜態和 Autostatic 路由
description: 通常會透過路由通訊協定動態取得遠端網路的路由。
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0206190c86c75e4e50ce390cf3f084db956671de6efebe21022151879362ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127828"
---
# <a name="static-and-autostatic-routes"></a>靜態和 Autostatic 路由

通常會透過路由通訊協定動態取得遠端網路的路由。 不過，系統管理員也可以藉由手動提供路由來 *植* 入路由表。 這些路由稱為 *靜態*。 靜態路由與代表遠端網路的介面相關聯。 與動態路由不同的是，即使重新開機路由器或停用介面，仍會保留靜態路由。

*Autostatic* 路由是透過路由通訊協定取得的，但取得的行為就像靜態路由一樣。 取得 autostatic 路由的程式如下所示： IP 或 IPX 路由器管理員發出要求，指出路由通訊協定會更新特定介面的路由資訊。 然後更新的結果會轉換成靜態路由。 請注意，只有特定路由通訊協定支援 autostatic 路由更新的要求。

 

 




