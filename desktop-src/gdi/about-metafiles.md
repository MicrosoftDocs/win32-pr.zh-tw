---
description: 就內部而言，中繼檔是稱為中繼檔記錄的可變長度結構陣列。
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: 關於中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc573d54f1f89e2dfe06edb8e225516fe8f0946485592d7d6aaea1faa651de85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779458"
---
# <a name="about-metafiles"></a>關於中繼檔

就內部而言，中繼檔是稱為 *中繼檔記錄* 的可變長度結構陣列。 中繼檔中的第一筆記錄會指定一般資訊，例如圖片建立所在的裝置解析度、圖片的大小等等。 其餘記錄（構成任何中繼檔的大量）會對應至圖形裝置介面， (需要用來繪製圖片的 GDI) 函數。 建立特殊的中繼檔裝置內容之後，這些記錄會儲存在中繼檔中。 然後，此中繼檔裝置內容會用於建立圖片所需的所有繪圖作業。 當系統處理與中繼檔 DC 相關聯的 GDI 函式時，它會將函式轉換為適當的資料，並將此資料儲存在附加至中繼檔的記錄中。

在圖片完成並將最後一筆記錄儲存在中繼檔中之後，您可以透過下列方式將中繼檔傳遞給另一個應用程式：

-   使用剪貼簿
-   將它內嵌在另一個檔案中
-   將其儲存在磁片上
-   重複播放

中繼檔會在其記錄轉換成裝置命令並由適當的裝置處理時 *播放* 。

中繼檔有兩種類型：

-   [增強格式的中繼檔](enhanced-format-metafiles.md)
-   [Windows 格式中繼檔](windows-format-metafiles.md)

 

 



