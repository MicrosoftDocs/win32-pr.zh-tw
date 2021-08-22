---
description: 若要記錄管理，您可以使用儲存在對等記錄結構中的資訊 \_ 。
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: 記錄管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a747ae16e1773fe5944f2e9afdde8377d5e100a9a91316f70bcd1be8db6cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011516"
---
# <a name="record-management"></a>記錄管理

若要記錄管理，您可以使用儲存在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record) 結構中的資訊。 當記錄建立、更新或刪除時，對圖表所做的變更會複寫到所有節點。 下表將識別更新和自動重新整理記錄的規則。



| 管理工作     | 規則                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 更新記錄   | 將到期時間保持不變或增加。 您無法縮短到期時間。                                                                                                                      |
| 重新整理記錄 | 使用 [**對等 \_ 記錄 \_ 旗標 \_ 自動重新整理**](/windows/desktop/api/P2P/ns-p2p-peer_record) 旗標來自動重新整理記錄。 只有當發行記錄的節點在線上時，才使用此旗標。 否則，請不要使用此旗標。 |



 

 

 



