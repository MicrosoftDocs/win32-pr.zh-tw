---
description: 我有一個包含 Windows Media 視訊資料流程的 AVI 檔。
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: 我有一個包含 Windows Media 視訊資料流程的 AVI 檔。 如何將它轉換成 WMV 檔案？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfc2a5980533487c7a1c8716806fcedda1c7147bdacaf3ea0c887acbff0f83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777138"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a>我有一個包含 Windows Media 視訊資料流程的 AVI 檔。 如何將它轉換成 WMV 檔案？

Windows Media 音訊和影片編解碼器介面未提供使用 Advanced Systems Format (ASF) （這是用於 WMV 檔案的格式）來建立檔案的方法。 如果您想要使用任何) 到 ASF 檔案的容器來轉換檔案 (，您必須使用 Windows 媒體格式 SDK 的物件。

從原始程式檔取出壓縮的 Windows 媒體範例，並將它們以資料流程範例形式傳遞至寫入器物件。 如需詳細資訊，請參閱 Windows 媒體格式9系列 SDK 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常見問題集](frequentlyaskedquestions.md)
</dt> </dl>

 

 



