---
title: 建立檔案或資料流程處理常式
description: 建立檔案或資料流程處理常式
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6732c572e390f3401f6e0472659bec7c522189b357b04d8ef7def20a7d9519b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785788"
---
# <a name="creating-a-file-or-stream-handler"></a>建立檔案或資料流程處理常式

在以 C 程式設計語言撰寫的應用程式中，檔案或資料流程處理常式通常會建立每個方法的函式。 您的應用程式會透過資料流程處理常式所建立的函式指標陣列來存取這些函式。 **IAVIStreamVtbl** 結構包含函式指標的陣列。 資料流程處理常式可以指派它想要為方法建立之函式的任何名稱。 結構中的函式指標位置表示函式與方法之間的對應。 例如，結構中的第一個函式指標會與 **QueryInterface** 方法相對應。 您的資料流程處理常式必須提供介面的所有功能。

 

 




