---
description: 若要取得路徑的元素，請呼叫 PdhParseCounterPath 函式。 函式會剖析計數器路徑的專案，並將它們傳回至 PDH \_ 計數器 \_ 路徑 \_ 元素結構中。
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: 從計數器路徑取得計數器路徑元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479c8df5c7176684fc439f632a22f829afe5afae202f7595579350450ee30c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143971"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>從計數器路徑取得計數器路徑元素

若要取得路徑的元素，請呼叫 [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) 函式。 函式會剖析計數器路徑的專案，並將它們傳回至 [**PDH \_ 計數器 \_ 路徑 \_ 元素**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) 結構中。

如果您有複雜的實例名稱 (其中一個包含父實例和實例索引) ，您可以呼叫 [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) 函數，以將實例名稱、實例索引和父系名稱解壓縮。

 

 



