---
description: PhoneClose 函式會關閉指定的電話裝置。
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: 關閉電話裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7e80f3a3869df8ff508d5f4b8d9cb05f493ea0bda4e8ff0ca619d46618e7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869449"
---
# <a name="closing-the-phone-device"></a>關閉電話裝置

[**PhoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)函式會關閉指定的電話裝置。 在使用者修改該電話的設定或其驅動程式之後，也可以強制關閉電話裝置。 如果使用者想要讓設定變更立即生效 (而不是在下一次系統重新開機) 後，它們會影響應用程式目前的裝置視圖 (例如裝置功能) 的變更，則服務提供者可以強制關閉電話裝置。

這些訊息也可以透過其他方式來回收電話裝置的結果來傳送。 因此，應用程式必須準備好處理未經要求的 [**電話 \_ 關閉**](phone-close.md) 訊息。 當手機裝置關閉時，就會隱藏與該裝置相關的任何未完成非同步回復。

 

 



