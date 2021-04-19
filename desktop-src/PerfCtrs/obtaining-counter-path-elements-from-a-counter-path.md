---
description: 若要取得路徑的元素，請呼叫 PdhParseCounterPath 函式。 函式會剖析計數器路徑的專案，並將它們傳回至 PDH \_ 計數器 \_ 路徑 \_ 元素結構中。
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: 從計數器路徑取得計數器路徑元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983639"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>從計數器路徑取得計數器路徑元素

若要取得路徑的元素，請呼叫 [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) 函式。 函式會剖析計數器路徑的專案，並將它們傳回至 [**PDH \_ 計數器 \_ 路徑 \_ 元素**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) 結構中。

如果您有複雜的實例名稱 (其中一個包含父實例和實例索引) ，您可以呼叫 [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) 函數，以將實例名稱、實例索引和父系名稱解壓縮。

 

 



