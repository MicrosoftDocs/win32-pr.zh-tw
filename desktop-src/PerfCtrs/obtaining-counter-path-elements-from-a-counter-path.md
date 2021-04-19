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
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a><span data-ttu-id="7211a-104">從計數器路徑取得計數器路徑元素</span><span class="sxs-lookup"><span data-stu-id="7211a-104">Obtaining Counter Path Elements from a Counter Path</span></span>

<span data-ttu-id="7211a-105">若要取得路徑的元素，請呼叫 [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) 函式。</span><span class="sxs-lookup"><span data-stu-id="7211a-105">To retrieve the elements of a path, call the [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) function.</span></span> <span data-ttu-id="7211a-106">函式會剖析計數器路徑的專案，並將它們傳回至 [**PDH \_ 計數器 \_ 路徑 \_ 元素**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) 結構中。</span><span class="sxs-lookup"><span data-stu-id="7211a-106">The function parses the elements of a counter path and returns them in a [**PDH\_COUNTER\_PATH\_ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) structure.</span></span>

<span data-ttu-id="7211a-107">如果您有複雜的實例名稱 (其中一個包含父實例和實例索引) ，您可以呼叫 [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) 函數，以將實例名稱、實例索引和父系名稱解壓縮。</span><span class="sxs-lookup"><span data-stu-id="7211a-107">If you have a complex instance name (one that contains a parent instance and instance index), you can call the [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) function to extract the instance name, instance index, and parent name.</span></span>

 

 



