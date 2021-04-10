---
description: RealTimeStylus、GestureRecognizer 和 DynamicRenderer 類別會實作為 COM 包裝函式，而且只能在 managed 程式碼中使用。
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: StylusInput Api 的執行注意事項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943261"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>StylusInput Api 的執行注意事項

[**RealTimeStylus**](realtimestylus-class.md)、 [GestureRecognizer](/previous-versions/ms575185(v=vs.100))和 [DYNAMICRENDERER](/previous-versions/ms575176(v=vs.100))類別會實作為 COM 包裝函式，而且只能在 managed 程式碼中使用。

當 [**realtimestylus**](realtimestylus-class.md)、 [GestureRecognizer](/previous-versions/ms575185(v=vs.100))或 [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) 物件以外掛程式的形式加入至 **realtimestylus** 物件時，基礎 com 物件就會在 COM 層級上互動。 因此，不支援直接呼叫 [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) 或 [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) 介面的方法。 將 **realtimestylus**、GestureRecognizer 或 DynamicRenderer 物件新增至 **realtimestylus** 物件是存取這些功能的唯一方法。

 

 
