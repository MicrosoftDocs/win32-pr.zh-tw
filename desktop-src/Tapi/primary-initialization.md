---
description: TAPI 應用程式必須呼叫初始化作業，這會從 TAPI 提示一連串動作，以及為應用程式設定通訊環境的服務提供者。
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: 主要初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae187692f1eb64546398a273bc823ab93f622b6a0472848c31f9d94b9ecd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060586"
---
# <a name="primary-initialization"></a>主要初始化

TAPI 應用程式必須呼叫初始化作業，這會從 TAPI 提示一連串動作，以及為應用程式設定通訊環境的服務提供者。

-   初始化是同步的，且在作業完成或失敗之前都不會傳回。
-   如果 TAPISRV 尚未執行，TAPI 會啟動它。
-   TAPI 會設定 TAPISRV 程式的連接。
-   TAPISVR 會載入登錄中指定的服務提供者，並提示他們將其支援的裝置初始化。

**TAPI 2.x：** 應用程式會藉由呼叫 [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)來執行初始化。

**TAPI 3.x：** 應用程式會呼叫 [**ITTAPI：： Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)。

 

 
