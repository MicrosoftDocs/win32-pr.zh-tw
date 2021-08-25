---
description: 資訊 DC 可用來取出預設裝置資料。
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: 資訊裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974b861f47ffbd19566a5224d0c2705e9797e86abbe46005c6eb1687a9573378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779128"
---
# <a name="information-device-contexts"></a>資訊裝置內容

資訊 DC 可用來取出預設裝置資料。 例如，應用程式可以呼叫 [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) 函式來建立特定印表機模型的資訊 DC，然後呼叫 [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) 和 [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) 函數來抓取預設的畫筆或筆刷屬性。 因為系統可以在不建立通常與其他類型的裝置內容相關聯的結構的情況下，取得裝置資訊，所以資訊 DC 所牽涉到的額外負荷較低，而且建立速度明顯比其他任何類型更快。 當應用程式使用資訊 DC 來完成資料的取出之後，必須呼叫 [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) 函數。

 

 



