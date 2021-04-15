---
description: 音訊和子圖片串流
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: 音訊和子圖片串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467895"
---
# <a name="audio-and-subpicture-streams"></a>音訊和子圖片串流

DVD-Video 光碟最多可有八個音訊串流（編號為0到7），每個串流都有最多六個不同的通道。  (請注意，音訊和子圖片串流的編號是從零開始，而標題、角度和家長能從1開始編號。 ) 在任何指定時間都只能選取其中一個串流。 針對 subpictures，最多可使用32串流，但在任何特定時間都只能啟用一個資料流程。 光碟通常是以預設的音訊和子圖片串流來撰寫，但應用程式可以讓使用者查看所有可用資料流程的清單，然後選取所需語言的清單。 此程式中的基本步驟在音訊和子圖片串流中都相同。

1.  決定可供標題使用的資料流程數目。
2.  逐一查看串流，並取得每個資料流程的資料流程屬性。
3.  從傳回的地區設定識別碼中取出語言代碼 (LCID) 並建立人們可讀取的字串。
4.  填入清單方塊或其他使用者介面 (UI) 控制項，讓使用者選取慣用的資料流程。

在 DVD 範例應用程式中，對話方塊中的 CAudioLangDlg：： MakeAudioStreamList 方法會示範基本步驟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



