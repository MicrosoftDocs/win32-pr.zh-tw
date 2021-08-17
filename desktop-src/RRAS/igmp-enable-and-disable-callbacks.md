---
title: IGMP 啟用和停用回呼
description: 多播群組管理員會使用兩個對 IGMP 的回呼，以協調介面擁有權從 IGMP 到路由通訊協定的變更，以及從路由通訊協定到 IGMP 的變更。
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103a0f9abb4d2a78b2b87fde3cb5832b4e88eb2677851d9fe703e5162263642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791141"
---
# <a name="igmp-enable-and-disable-callbacks"></a>IGMP 啟用和停用回呼

多播群組管理員會使用兩個對 IGMP 的回呼，以協調介面擁有權從 IGMP 到路由通訊協定的變更，以及從路由通訊協定到 IGMP 的變更。 回呼可讓 IGMP 並存于具有另一個路由通訊協定的介面上，例如 DVMRP。

在介面擁有權變更之後，多播群組管理員會先叫用 [**PMGM \_ 停用 \_ IGMP \_ 回呼**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) 回呼。 在多播群組管理員叫用 [**PMGM \_ 啟用 \_ IGMP \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) 回呼之前，IGMP 必須停止新增和刪除指定介面上的群組成員資格。

當介面擁有權變更完成後，多播群組管理員會叫用 [**PMGM \_ 啟用 \_ IGMP \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) 回呼。

 

 