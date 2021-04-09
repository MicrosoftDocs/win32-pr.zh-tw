---
title: RPF 警示回呼
description: 當多播群組管理員收到來自新來源的封包或來自新群組的封包的通知之後，多播群組管理員會在路由表的多播視圖中查閱來源的路由。
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675976"
---
# <a name="rpf-alert-callbacks"></a>RPF 警示回呼

當多播群組管理員收到來自新來源的封包或來自新群組的封包的通知之後，多播群組管理員會在路由表的多播視圖中查閱來源的路由。 然後，多播群組管理員會叫用 [**PMGM \_ RPF \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) 回呼給擁有資料抵達介面的通訊協定。

叫用此回呼之後，如果路由通訊協定必須在不同的介面上接收群組的資料，路由通訊協定就可以變更傳入的介面。

 

 




