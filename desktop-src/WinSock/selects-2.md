---
description: 在原始的 Berkeley Software 散發 (BSD) 通訊端介面，select 函式是標準的 (，而且只有) 的方法可取得網路事件指示。
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: 選擇
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c075d2b8b18de79c25852eb0949cc727a8f3474e39392cf6e0a50fc60390d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740920"
---
# <a name="selects"></a>選擇

在原始的 Berkeley Software 散發 (BSD) 通訊端介面， [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式是標準的 (，而且只有) 的方法可取得網路事件指示。 針對每個通訊端，可輪詢或等候讀取、寫入或錯誤狀態的相關資訊。 如需詳細資訊，請參閱 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) 。 請注意， \_ 此方法無法取得網路事件 FD QOS。

 

 
