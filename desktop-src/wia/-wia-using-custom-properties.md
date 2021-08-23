---
description: 使用自訂屬性。
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: 使用自訂屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee01bc0df80acecec9805ea15cd8da65fa23a441c9c7818a88223aa47b963d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813628"
---
# <a name="using-custom-properties"></a>使用自訂屬性

**使用自訂屬性**。

Windows 映像取得 (WIA) 驅動程式可以定義自己的自訂屬性。 呼叫端可以操作自訂屬性，就像一般的 WIA 屬性一樣。 不過，只有您的應用程式或自訂 UI 模組可以存取這些自訂屬性。

WIA 驅動程式應該將自訂屬性定義為具有裝置屬性的 WIA 私用 DEVPROP 所位移的屬性識別碼 \_ \_ ，並 \_ \_ 針對一般專案屬性使用 wia 私用 ITEMPROP，例如 [IWiaMiniDrv 內：:d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx)。 如需詳細資訊，請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)。

有兩種方式可以將自訂參數傳遞給 WIA 驅動程式。

第一個選項是使用 **IWiaItemExtras：： Escape** 方法 () 的 Platform SDK 檔中所述。 這類似于 [IStiUSD：： Escape](https://msdn.microsoft.com/library/ms794396.aspx) 方法，但它可讓呼叫者直接使用 WIA，而不是使用 STI 方法。 您可以使用 **IWiaItemExtras：： Escape** 將任何資訊傳遞至驅動程式，而驅動程式可以將任何資訊傳遞回來。 WIA 服務只會管理呼叫端與驅動程式之間傳遞的緩衝區。

第二個選項是使用自訂屬性。 使用 **IWiaItemExtras：： Escape** 方法比使用自訂 wia 屬性更有彈性，但自訂 wia 屬性可讓您將資訊儲存在專案的屬性資料流程中，以便驅動程式可以在其他時間讀取資訊。

 

 



