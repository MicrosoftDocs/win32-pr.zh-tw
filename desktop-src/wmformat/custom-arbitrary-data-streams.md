---
title: 自訂任意資料流程
description: 自訂任意資料流程
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK，自訂任意資料流程
- Advanced Systems Format (ASF) 、自訂任意資料流程
- ASF (Advanced Systems Format) ，自訂任意資料流程
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 自訂任意資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968258"
---
# <a name="custom-arbitrary-data-streams"></a>自訂任意資料流程

您可以在 ASF 檔案中建立資料流程，以包含任何資料類型。 如果任何支援的資料流程類型都不符合您的需求，您必須使用任意資料流程。 寫入器物件會處理任意資料流程，就像處理任何未壓縮的資料流程一樣;這些範例會從檔案的資料區段中的其他資料流程 packetized 和結合範例。 當然，只有經過特別設計來處理任意類型的讀取應用程式，才能在讀取物件傳遞之後處理資料。

任意資料流程的常見用法之一，是針對使用協力廠商編解碼器編碼的媒體資料。 因為此 SDK 的物件不會直接與協力廠商編解碼器互動，所以您的撰寫應用程式必須使用編解碼器的編碼部分來處理範例，並將壓縮的範例傳遞給寫入器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**任意資料流程**](arbitrary-streams.md)
</dt> <dt>

[**設定自訂任意資料流程**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




