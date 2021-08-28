---
title: 節點節點配置和解除配置
description: 由存根進行的節點依節點配置和解除配置資料結構是用戶端和伺服器上所有參數的預設記憶體管理方法。
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52aea7c2e95615af8549c1f66476e1a105b91abd68dd31089db9cf23d8ec2af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927837"
---
# <a name="node-by-node-allocation-and-deallocation"></a>節點節點配置和解除配置

由存根進行的節點依節點配置和解除配置資料結構是用戶端和伺服器上所有參數的預設記憶體管理方法。 在用戶端上，存根會使用對 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1)的個別呼叫來配置每個節點。 在伺服器端，您可以盡可能使用私用記憶體，而不是呼叫 **midl \_ 使用者 \_ 配置**。 如果呼叫 **midl \_ 使用者 \_ 配置** ，伺服器 stub 會呼叫 **midl \_ 使用者 \_ free** 來釋出資料。 在大部分的情況下，使用節點對節點的配置和解除配置，而不使用 **\[ 配置 (所有 \_ 節點) \]** 將會導致伺服器端存根的效能提升。

 

 