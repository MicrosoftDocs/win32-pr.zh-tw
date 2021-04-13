---
description: 裝置標記法
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: 裝置標記法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468956"
---
# <a name="device-representation"></a>裝置標記法

裝置有兩個主要的行為，可由 Windows 可攜式裝置 (WPD) 架構來解決：

-   存取和儲存內容。 例如，應用程式必須能夠將音樂檔新增到便攜音樂播放機。
-   裝置的程式設計。 這包括簡單的作業，例如變更設定和準備裝置以進行資料捕獲，或更複雜的作業，例如上傳固件。 範例包括將「拍攝」命令發出至數位的靜止相機。

在 WPD 中，這些行為的描述方式是將裝置表示為物件的階層。 下圖顯示多函式裝置的 WPD 物件標記法，在此案例中為行動電話。

![顯示行動電話物件階層的圖例](images/wpd-overview-figure3.gif)

此階層說明下列功能和內容。

功能：

-   儲存體物件。 此裝置具有資料存放區。
-   連絡人服務。 這項服務是一個功能物件，可用來同步處理和儲存手機上的連絡人。
-   SMS 服務。 這項服務是一個功能物件，可用來傳送、接收和儲存 SMS 訊息。

內容: 

-   媒體物件。 此裝置會將影像、音樂和影片檔案儲存在儲存物件上的資料夾中。 雖然圖中顯示的檔案是儲存在一個資料夾下，裝置也可以將內容細分為依儲存的媒體類型組織的資料夾;例如，[影像資料夾]、[音樂] 資料夾和 [影片] 資料夾。
-   Contact 物件。 此裝置會將連絡人資訊儲存 (例如姓名、電話號碼和位址) 作為連絡人服務的子系
-   Message 物件。 此裝置會將 SMS 訊息儲存為 SMS 服務的子系。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式總覽**](application-overview.md)
</dt> </dl>

 

 



