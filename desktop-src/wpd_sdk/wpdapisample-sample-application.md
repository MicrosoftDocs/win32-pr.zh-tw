---
description: WpdApiSample 應用程式
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: WpdApiSample 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690268"
---
# <a name="wpdapisample-application"></a>WpdApiSample 應用程式

WpdApiSample 範例應用程式是一個命令列桌面應用程式，可讓您列舉連線的裝置、探索裝置、查詢屬性和屬性的物件、傳送和取出物件等等。 在啟動時，應用程式會開啟一個命令視窗，其中會列出您可以執行的工作。

WpdApiSample 範例應用程式包含下列檔案：



| **檔案**               | **說明**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration .cpp | 包含列舉裝置上所有物件的函式。                                                                                                                                            |
| ContentProperties .cpp  | 包含函式，這些函式會讀取和寫入物件屬性，並建立大量屬性集/get 要求。                                                                                                         |
| ContentTransfer .cpp    | 包含在裝置上傳送內容、讀取物件類型需求，以及在裝置上建立資料夾的函式。                                                                         |
| DeviceCapabilities .cpp | 包含函式，用來列出裝置上的功能物件類型、列出每個功能物件類型所支援的內容類型，以及顯示呈現物件設定檔。                             |
| DeviceEnumeration .cpp  | 列出所有已連線裝置的易記名稱、製造商和描述。                                                                                                                       |
| DeviceEvents .cpp       | 包含會在每次引發事件時記錄裝置事件及其參數的函式。                                                                                                                 |
| stdafx.cpp             | 包含標準檔案。                                                                                                                                                                              |
| WpdApiSample .cpp       | 裝載 **\_ tmain** 啟動函式，此函式會呼叫本機 **DoMenu** 函式，此函式會顯示可用裝置和工作的清單，並呼叫適用于使用者功能表選取的函式。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例](sample.md)
</dt> </dl>

 

 



