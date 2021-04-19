---
description: WpdServicesApiSample 應用程式
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: WpdServicesApiSample 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987549"
---
# <a name="wpdservicesapisample-application"></a>WpdServicesApiSample 應用程式

裝置服務是功能物件的擴充功能：除了以邏輯方式分組裝置功能之外，裝置服務也提供應用程式以程式設計方式探索這些功能的能力。

WpdServicesApiSample 範例應用程式是一個命令列桌面應用程式，可讓您在連接到電腦的裝置上探索連絡人服務。 您可以藉由列出支援的方式來探索這些服務：格式、事件、方法和抽象服務。 您也可以使用此應用程式抓取指定連絡人服務上的屬性，並叫用該服務所支援的方法。

如果您還沒有支援「連絡人」服務的裝置，您仍然可以在第一次安裝 Windows 驅動程式套件中包含的 WpdServiceSampleDriver 時執行 WpdServicesApiSample。

WpdServicesApiSample 範例應用程式包含下列檔案：



| **檔案**                | **說明**                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration .cpp  | 包含列舉指定連絡人服務上之內容的方法。                                                                                                                                  |
| ContentProperties .cpp   | 包含在指定的連絡人服務上讀取和寫入屬性的方法。                                                                                                                              |
| ServiceCapabilities .cpp | 包含方法，這些方法會取得所指定連絡人服務所支援的支援格式、事件和抽象服務。                                                                   |
| ServiceEnumeration .cpp  | 包含可抓取裝置資訊的 helper 函式，例如裝置易記名稱或支援的連絡人服務。                                                                       |
| ServiceMethods .cpp      | 包含方法，這些方法會取出並叫用指定連絡人服務所支援的方法。                                                                                                              |
| stdafx.cpp              | 包含標準檔案。                                                                                                                                                                              |
| WpdServiceApiSample .cpp | 裝載 **\_ tmain** 啟動函式，此函式會呼叫本機 **DoMenu** 函式，此函式會顯示可用裝置和工作的清單，並呼叫適用于使用者功能表選取的函式。 |



 


## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例](sample.md)
</dt> </dl>

 

 



