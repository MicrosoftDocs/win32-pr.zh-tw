---
description: 您可以使用 EscapeCommFunction 函式，針對裝置呼叫某些通訊功能。
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: 擴充函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913feb46f61777bcb07fda1639519c4ef04fcb4905075b1c67955a3e911b9d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405333"
---
# <a name="extended-functions"></a>擴充函數

您可以使用 [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) 函式，針對裝置呼叫某些通訊功能。 此函式會傳送程式碼，以指示裝置執行擴充功能。 例如，應用程式可以使用 SETBREAK 碼暫停字元傳輸，並使用 CLRBREAK 程式碼繼續傳輸。 您也可以藉由呼叫 [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) 和 [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) 函數來啟動這些特定作業。 **EscapeCommFunction** 也可以用來執行手動數據機控制。 例如，CLRDTR 和 SETDTR 碼可以用來實 (資料終端機) 流量控制的手動 DTR。 不過，請注意，如果在裝置設定為啟用 DTR 握手時，進程使用 **EscapeCommFunction** 來操作 dtr 行，或如果啟用了 rts 握手，)  (則會發生錯誤。

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)函式可讓程式將擴充的函式程式碼直接傳送到指定的設備磁碟機，使裝置執行指定的作業。 **DeviceIoControl** 會提供與標準串列通訊功能不支援的通訊資源功能相關聯的裝置。 它可讓應用程式使用該裝置特有的參數來設定裝置，以及呼叫任何裝置特定的函式。

 

 
