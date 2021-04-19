---
description: 雖然 \# \# Tablet PC 平臺無法同時在兩個執行緒上存取&160; 辨識器內容&160; 但是 AdviseInkChange 函式可以隨時在任何執行緒上呼叫。
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: 辨識器執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992071"
---
# <a name="recognizer-threading-considerations"></a>辨識器執行緒考慮

雖然 Tablet PC 平臺無法同時存取兩個執行緒上的辨識 [器內容](hrecocontext-handle.md) ，但可以在任何執行緒上隨時呼叫 [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) 函數。 因為 Tablet PC 平臺無法確保一次只有一個辨識器內容，所以個別執行緒中有兩個不同的辨識器內容可能會同時嘗試存取您的辨識 [器](hrecognizer-handle.md)。 因此，您的辨識引擎中的全域變數必須是安全線程。

單字清單是用來提高精確度的選擇性執行。 如果您的辨識器會實作為字組清單，它必須是安全線程。 如需使用 word 清單的詳細資訊，請參閱 [使用應用程式字典](using-application-dictionaries.md)。

如需其他執行緒考慮的詳細資訊，請參閱 [TABLET PC 執行緒的考慮](tablet-pc-threading-considerations.md)。

 

 



