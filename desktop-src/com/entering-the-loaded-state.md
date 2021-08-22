---
title: 進入載入的狀態
description: 進入載入的狀態
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091d9fe92acbf202c40c1a7ec485f3028bbc22d652ef29db1cb406d961b19e7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410248"
---
# <a name="entering-the-loaded-state"></a>進入載入的狀態

當物件進入載入的狀態時，就會建立代表物件的記憶體內結構，以便在其上叫用作業。 載入物件的處理常式或同進程伺服器。 從持續性儲存體載入物件 (從被動轉換到載入的) 狀態，或第一次建立物件時，會發生這個進程（稱為具現 *化*）。

就內部而言，具現化是兩階段的程式。 系統會建立適當類別的物件，之後呼叫該物件上的方法來執行初始化，並授與物件資料的存取權。 初始化方法是在物件的其中一個支援的介面中定義。 呼叫的特定初始化方法取決於要具現化物件的內容，以及初始化資料的位置。

 

 




