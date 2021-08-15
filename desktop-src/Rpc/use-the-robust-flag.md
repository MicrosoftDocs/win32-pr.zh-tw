---
title: 使用/robust 旗標
description: 一律使用/robust 參數編譯 .idl 檔。
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3d6a7c93cbd97e2c65cc83e6933b3204dddbcf2c0e088dfbc0d98bbdb6628d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010886"
---
# <a name="use-the-robust-flag"></a>使用/robust 旗標

一律使用 [**/robust**](/windows/desktop/Midl/-robust) 參數編譯 .idl 檔。 使用 **/robust** 參數會產生額外的資訊，讓網路資料表示 (NDR) 引擎，以在動態陣列、等位和 COM 和 RPC 應用程式的輸出介面指標中的相互關聯引數上執行執行時間錯誤檢查。 如果軟體無法使用此旗標進行編譯，軟體就會暴露在攻擊中，而不會在任何其他區域中進行保護。

 

 