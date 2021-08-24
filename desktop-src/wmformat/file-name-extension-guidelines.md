---
title: 檔案名延伸指導方針
description: 檔案名延伸指導方針
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows媒體格式 SDK，副檔名
- Advanced Systems Format (ASF) 、副檔名
- ASF (Advanced 系統格式) 、副檔名
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ccd8c3b1b4ba27aa7360296fc336625cb0f51c4374bb77c06d349cb70a987c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704001"
---
# <a name="file-name-extension-guidelines"></a>檔案名延伸指導方針

副檔名會提供獨立軟體廠商，包含使用該特定延伸的應用程式呈現需求的相關資訊。

您必須針對以 Windows 媒體格式 SDK 為基礎的應用程式所建立的檔案使用的副檔名，取決於檔案中的內容類型。 使用下列邏輯來決定您必須使用的副檔名。

如果檔案包含任何使用協力廠商編解碼器編碼的資料流程或任何不支援的未壓縮資料 (包括任意資料) ，則檔案必須使用 .asf 副檔名。

如果檔案未包含不支援的資料流程，並包含一或多個未壓縮或以任何 Windows 媒體視頻編碼器編碼的影片串流，則檔案必須使用 .wmv 副檔名。 這些檔案也可能包含 PCM 音訊串流、以任何 Windows 媒體音訊編解碼器、腳本串流和 Web 串流編碼的音訊串流。

如果檔案未包含不支援的資料流程且沒有支援的視頻串流，且包含一或多個音訊串流未壓縮的 PCM 或使用任何 Windows 媒體音訊編解碼器編碼，則檔案必須使用 .wma 副檔名。 這些檔案也可以包含腳本資料流程和 Web 資料流程。

如果檔案只包含非音訊或影片的資料流程，則必須使用 .asf 副檔名。

支援的未壓縮影片類型包括 RGB8、RGB565、RGB555、RGB24、RGB32、I420、IYUV、YV12、YUY2、UYVY、YVYU 和 YVU9。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Project考慮**](project-considerations.md)
</dt> </dl>

 

 




