---
title: 基本和命令
description: 基本和命令
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL、基本
- OpenGL、命令
- 基本 OpenGL
- 命令 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0729b71e9c25abf22045884910fcec3780d50aff2fe94dbe485f83f640cdeced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888058"
---
# <a name="primitives-and-commands"></a>基本和命令

OpenGL 會繪製 *基本* 點、線段或 polygonssubject 至數個可選取的模式。 您可以單獨控制模式。 也就是說，設定一個模式不會影響是否已設定其他模式 (雖然許多模式可能會進行互動，以判斷最終畫面格緩衝區) 的結果。 若要指定基本、設定模式和執行其他 OpenGL 作業，請以函式呼叫的形式發出命令。

基本專案是由一或多個 *頂點* 的群組所定義。 頂點會定義點、線條的端點，或兩個邊符合的多邊形角落。 由頂點座標、色彩、法線、材質座標和邊緣旗標所組成的資料 () 與頂點相關聯，而且每個頂點和其相關聯的資料會以相同方式分別以連續處理。 這項規則的唯一例外狀況是必須裁剪頂點群組，讓特定的基本型別符合指定區域的情況。 在此情況下，可能會修改頂點資料並建立新頂點。 裁剪的類型取決於頂點群組所代表的基本物件。

命令一律會依照接收的順序進行處理，但在命令生效之前可能會有不定的延遲。 這表示每個基本型別會在任何後續的命令生效之前完全繪製。 這也表示狀態查詢命令會傳回與所有先前發行之 OpenGL 命令的完整執行一致的資料。

 

 




