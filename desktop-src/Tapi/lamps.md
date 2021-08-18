---
description: 手機裝置上的燈可能會以各種不同的光源模式亮起。
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: 燈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150e499dbd66ca772d35855c4cdb086bbb1ecc12617f55bcd33dccf8435e8771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762282"
---
# <a name="lamps"></a>燈

手機裝置上的燈可能會以各種不同的光源模式亮起。 與響鈴模式不同的是，燈泡模式在不同廠商的不同電話組間是更一致的。 API 會定義一組常見的燈泡模式。 以燈泡按鈕識別碼識別的燈泡，可在指定的燈泡模式中亮起。 燈泡也可以查詢其目前的燈泡模式。

用於燈的 TAPI 函式是 [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp)，它會在指定的燈光源模式中，以指定的開啟電話裝置燈燈燈，而 [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp)則會傳回指定燈的目前燈泡模式。

當手機裝置的燈泡變更時，會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。 此訊息的參數提供了變更的指示。

 

 



