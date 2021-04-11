---
title: 接收器
description: 接收器
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media 格式 SDK，接收
- Windows Media Format SDK，file 接收
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- Advanced Systems Format (ASF) ，file 接收
- ASF (Advanced Systems Format) ，file 接收
- Windows Media Format SDK，網路接收器
- Windows Media Format SDK、push 接收器
- Advanced Systems Format (ASF) ，網路接收器
- ASF (Advanced Systems Format) ，網路接收器
- Advanced Systems Format (ASF) 、push 接收器
- ASF (Advanced 系統格式) 、推播接收
- 接收、關於
- 檔接收，關於
- 網路接收器
- 推播接收器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023066"
---
# <a name="sinks"></a>接收器

Windows Media 格式 SDK 的寫入器物件會將已處理的內容傳遞給接收。 每個接收都是可傳遞資料的物件。 傳遞點取決於接收的類型。 有三種類型的接收：檔案接收、網路接收和推播接收。

## <a name="file-sinks"></a>檔案接收

File 接收會將 ASF 內容寫入本機或網路磁碟機機上的檔案。 當您使用 writer 物件來寫入檔案，但未明確地新增檔案接收時，寫入器會使用您傳遞給 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)的名稱來為您建立一個檔案。 您可以將多個檔案接收指派給寫入器物件，以便一次寫入數個檔案中的內容。

藉由使用檔案接收，您可以控制檔案的許多層面。 下列功能可透過 file 接收取得。

-   檔案統計資料監視。 您可以在建立檔案時，監視檔案的大小和持續時間。
-   部分內容檔案建立。 檔案接收可以設定為在特定時間開始寫入內容，並在特定時間結束寫入。 這可讓您在相同的寫入行程中，建立多個檔案，其中包含相同內容的不同區段。

## <a name="network-sinks"></a>網路接收器

網路接收會將內容廣播到網路位址。 讀取用戶端可以連接到位址以接收廣播。

## <a name="push-sinks"></a>推播接收器

推播接收會將內容從寫入器傳遞至執行 Windows Media Services 的伺服器。 推播接收器通常用於一部電腦編碼即時內容，並將它傳遞給一或多部伺服器進行廣泛散發的案例。 使用推播接收可讓您將電腦專用於特定工作，以節省每部伺服器的頻寬和處理能力。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案寫入功能**](file-writing-features.md)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 




