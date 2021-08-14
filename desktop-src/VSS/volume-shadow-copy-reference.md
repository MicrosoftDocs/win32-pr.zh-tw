---
description: 磁碟區陰影複製服務 (VSS) 是一組 COM 和 c + + Api，可讓您在系統上的應用程式 (呼叫寫入器時執行磁片區備份，) 繼續寫入磁片區。
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: 磁片區陰影複製 API 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbc2d0bec6d68572a67a1dc80327fb80028d7f8d98487f24fec24e2c2e65f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751525"
---
# <a name="volume-shadow-copy-api-reference"></a>磁片區陰影複製 API 參考

磁碟區陰影複製服務 (VSS) 是一組 COM 和 c + + Api，可讓您在系統上的應用程式 (呼叫寫入器時執行磁片區備份，) 繼續寫入磁片區。

VSS 透過建立陰影複製，在指定的時間點複製原始磁片區，以支援這些備份。

協力廠商開發人員可以使用 VSS API 來建立要求者 (例如備份應用程式) 建立及管理陰影複製。

建立和表示陰影複製的實際工作，是由稱為提供者的系統層級應用程式進行。

開發人員也可以使用 API 來設計寫入器：可透過 VSS 感知的應用程式，使用陰影複製的建立和操作來協調 i/o 作業。

-   [磁片區陰影複製 API 類別](volume-shadow-copy-api-classes.md)
-   [磁片區陰影複製 API 資料類型](volume-shadow-copy-api-data-types.md)
-   [磁片區陰影複製 API 列舉](volume-shadow-copy-api-enumeration-types.md)
-   [磁片區陰影複製 API 函數](volume-shadow-copy-api-functions.md)
-   [磁片區陰影複製 API 介面](volume-shadow-copy-api-interfaces.md)
-   [磁片區陰影複製 API 結構](volume-shadow-copy-api-structures.md)
-   [磁片區陰影複製詞彙](volume-shadow-copy-glossary.md)

如需撰寫要求者和寫入器的詳細資訊，請參閱 [使用磁碟區陰影複製服務](using-the-volume-shadow-copy-service.md)。

 

 



