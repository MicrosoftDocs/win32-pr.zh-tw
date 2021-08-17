---
description: 記憶體管理員會建立下列記憶體集區，供系統用來配置記憶體：非分頁集區和分頁集區。
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: 記憶體集區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a49597cf90324395c50a4e44aac03815426f0c1de8ea2c7ca7aa85b5cdac95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808995"
---
# <a name="memory-pools"></a>記憶體集區

記憶體管理員會建立下列記憶體集區，供系統用來配置記憶體：非分頁集區和分頁集區。 這兩個記憶體集區都位於為系統保留的位址空間區域中，並對應至每個進程的虛擬位址空間。 非分頁集區包含保證存在於實體記憶體中的虛擬記憶體位址（只要配置了對應的核心物件）。 分頁集區是由可在系統中傳入和傳出的虛擬記憶體所組成。 為了改善效能，具有單處理器的系統有三個分頁集區，而多處理器系統有五個分頁集區。

[核心物件](../sysinfo/kernel-objects.md)的控制碼會儲存在分頁集區中，因此您可以建立的控制碼數目是以可用的記憶體為基礎。

系統會記錄其非分頁集區、分頁集區和分頁檔案使用方式的限制和目前值。 如需詳細資訊，請參閱 [記憶體效能資訊](memory-performance-information.md)。

 

 
