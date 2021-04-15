---
title: 視窗回呼服務
description: 視窗回呼服務
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- 多媒體音訊、視窗回呼服務
- 音訊、視窗回呼服務
- 音訊 mixers，視窗回呼服務
- mixers，視窗回呼服務
- 視窗回呼服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463072"
---
# <a name="window-callback-services"></a>視窗回呼服務

混音器服務提供視窗回呼服務，讓您的應用程式可以處理來自混音器驅動程式的訊息。 若要使用這些服務，請在 \_ *fdwOpen* 參數中指定回呼視窗旗標，並在 [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)函數的 *dwCallback* 參數中指定視窗控制碼。 驅動程式訊息會傳送至 *dwCallback* 中的控制碼所識別之視窗的視窗程式函式。 這些訊息是音訊裝置類型的特定訊息。

 

 