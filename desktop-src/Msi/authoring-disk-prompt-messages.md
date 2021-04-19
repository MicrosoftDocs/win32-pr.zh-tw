---
description: 您可以使用下列指導方針來撰寫 Windows Installer 安裝，此安裝程式會顯示訊息方塊，以提示使用者插入磁片。
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: 撰寫磁片提示訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989363"
---
# <a name="authoring-disk-prompt-messages"></a>撰寫磁片提示訊息

您可以使用下列指導方針來撰寫 Windows Installer 安裝，此安裝程式會顯示訊息方塊，以提示使用者插入磁片。

**若要顯示訊息方塊以提示使用者插入磁片**

1.  您可以使用安裝程式的撰寫功能，在 [屬性](property-table.md)表中設定 [**DiskPrompt**](diskprompt.md)屬性字串。 這應該包含要安裝的產品名稱，以及在磁片上列印的標題字串內的預留位置參數。 例如，針對 Microsoft Publisher， **DiskPrompt** 屬性可能是「Microsoft Publisher： disk \[ 1」 \] ，其中 \[ 1 \] 是磁片標題的預留位置。
2.  輸入每個磁片的標題，以提示輸入 [媒體](media-table.md) 資料表中 DiskPrompt 資料行的個別資料列。 例如，媒體資料表中的第一個和唯一一個專案可能是「1–安裝」。
3.  在 [InstallFiles](installfiles-action.md) 動作期間， [媒體](media-table.md) 資料表 DiskPrompt 資料行中的值會取代為 [**DiskPrompt**](diskprompt.md) 屬性字串中的預留位置。
4.  訊息方塊所顯示的訊息是從 [錯誤資料表](error-table.md)內建的範本字串所建立。 這是錯誤1302，範本字串為：「請插入磁片：2」 \[ \] ，而 \[ 2 \] 代表 [**DiskPrompt**](diskprompt.md) 屬性的預留位置。

此範例會對使用者顯示下列訊息：「請插入磁片： Microsoft Publisher： Disk 1 – Install」。

請注意，除了 [無] 以外的所有 [消費者介面層級](user-interface-levels.md) ，都會顯示磁片提示訊息。

 

 



