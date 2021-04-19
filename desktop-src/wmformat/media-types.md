---
title: Windows Media 格式 SDK 的媒體類型
description: 瞭解 Windows Media Format SDK 可以使用的媒體類型。 媒體類型是指派給 SDK 中常數的 GUID 值。
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK，媒體類型
- Advanced Systems Format (ASF) 、媒體類型
- ASF (Advanced 系統格式) 、媒體類型
- 媒體類型，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106978549"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Windows Media 格式 SDK 的媒體類型

媒體類型可識別 Windows Media Format SDK 可以使用的不同類型媒體。 所有媒體類型都是已指派給 SDK 中常數的 GUID 值。 本章節所列的常數所代表的 GUID 值，會列在此參考的 [ [媒體類型識別碼](media-type-identifiers.md) ] 區段中。

下表列出主要的媒體類型。 這些常數會定義 Windows Media 格式 SDK 所支援之數位媒體的高階分類。



| 主要類型                | Description                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| WMMEDIATYPE \_ 影片        | 影片串流。                                                                                         |
| WMMEDIATYPE \_ 音訊        | 音訊串流。                                                                                        |
| WMMEDIATYPE \_ 腳本       | 腳本資料流程。                                                                                        |
| WMMEDIATYPE \_ FileTransfer | 包含資料檔案的資料流程。 包含 HTML 檔案的 Web 串流也有此主要類型。 |
| WMMEDIATYPE \_ 影像        | 說明的音訊檔案的 JPEG 影像串流 (如投影片放映) 所示。                                 |
| WMMEDIATYPE \_ 文字         | 文字資料流程。                                                                                          |



 

除了明確支援的主要媒體類型之外，您還可以建立自己的任意資料類型。 針對自訂任意資料類型，您必須確定您使用的 GUID 不符合現有的主要類型。

除了主要類型之外，媒體資料流程通常會有子類型。 下列各節列出支援的子類型。



| 區段                                                        | 描述                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [未壓縮的媒體子類型](uncompressed-media-subtypes.md) | 描述適用于未壓縮媒體的子類型。 這些類型通常與輸入或輸出媒體相關聯。              |
| [壓縮的媒體子類型](compressed-media-subtypes.md)     | 描述適用于壓縮媒體的子類型。 這些類型通常與 ASF 檔案內串流中的媒體相關聯。 |
| [影片輸入格式](video-input-formats.md)                 | 列出接受 Windows Media 視訊9編解碼器輸入的影片格式。                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體類型識別碼**](media-type-identifiers.md)
</dt> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 




