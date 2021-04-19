---
description: 在原始的 Berkeley Software 散發 (BSD) 通訊端介面，select 函式是標準的 (，而且只有) 的方法可取得網路事件指示。
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: 選擇
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969280"
---
# <a name="selects"></a>選擇

在原始的 Berkeley Software 散發 (BSD) 通訊端介面， [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式是標準的 (，而且只有) 的方法可取得網路事件指示。 針對每個通訊端，可輪詢或等候讀取、寫入或錯誤狀態的相關資訊。 如需詳細資訊，請參閱 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) 。 請注意， \_ 此方法無法取得網路事件 FD QOS。

 

 
