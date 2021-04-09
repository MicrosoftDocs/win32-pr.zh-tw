---
description: 手機裝置上的燈可能會以各種不同的光源模式亮起。
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: 燈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027278"
---
# <a name="lamps"></a>燈

手機裝置上的燈可能會以各種不同的光源模式亮起。 與響鈴模式不同的是，燈泡模式在不同廠商的不同電話組間是更一致的。 API 會定義一組常見的燈泡模式。 以燈泡按鈕識別碼識別的燈泡，可在指定的燈泡模式中亮起。 燈泡也可以查詢其目前的燈泡模式。

用於燈的 TAPI 函式是 [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp)，它會在指定的燈光源模式中，以指定的開啟電話裝置燈燈燈，而 [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp)則會傳回指定燈的目前燈泡模式。

當手機裝置的燈泡變更時，會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。 此訊息的參數提供了變更的指示。

 

 



