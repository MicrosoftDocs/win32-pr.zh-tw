---
description: 擴充性的達成方式是提供新的物件識別碼 (Oid) 、新的編碼類型和新的 Dll。
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: OID 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850851"
---
# <a name="oid-overview"></a>OID 總覽

擴充性的達成方式是提供新的 [*物件識別碼*](../secgloss/o-gly.md) (oid) 、新的編碼類型和新的 dll。

CryptoAPI Oid 可以採用下列任何形式：

-   數值字串，例如 "1.2.3.500.88"
-   英數位元字串，例如 *MyFunction*
-   值小於或等於0xFFFF 的常數。 這些常數通常會透過在標頭檔中使用 **\# define** 語句來與名稱產生關聯。

可擴充函式接受 OID 和編碼類型引數。 這些函式會搜尋系統登錄，以尋找與傳遞給函式的 OID 和編碼類型引數相關聯的 DLL。 如果已找到 OID 的 DLL、編碼類型組合，就會載入 DLL，並呼叫其函式。 下圖顯示此 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 函式的流程：

![oid 流程](images/oidflow.png)

這可讓 CryptoAPI 的功能隨著需求而擴充。 使用此方法會對新功能的開發人員造成負擔，以撰寫該功能的所有必要程式碼。 例如，若要編碼某些新的資料結構，DLL 中的函數必須執行整個編碼程式。

 

 
