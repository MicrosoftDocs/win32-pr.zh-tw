---
title: 音訊和影片串流
description: 音訊和影片串流
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows媒體格式 SDK，音訊串流
- Advanced Systems Format (ASF) 、音訊串流
- ASF (Advanced Systems Format) 、音訊串流
- Windows媒體格式 SDK、影片串流
- Advanced Systems Format (ASF) 、影片串流
- ASF (Advanced 系統格式) 、影片串流
- Windows媒體格式 SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 音訊串流，關於
- 影片串流，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bb1836540a8de3b0834d271c1aeb97ba2869fa5acfcd221d03071b32ec94e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705222"
---
# <a name="audio-and-video-streams"></a>音訊和影片串流

使用 Windows 媒體格式 SDK 所建立的檔案中最常見的資料流程類型是音訊和影片串流。 音訊和影片資料的數位表示很複雜，而且會佔用海量儲存體。 在大部分的情況下，音訊和影片都會先壓縮，然後再新增至 ASF 檔案。 壓縮會使用壓縮程式/解壓縮程式 (編解碼器) 來完成。

此 SDK 包含數個 Windows 媒體編解碼器，並為數字媒體提供絕佳的品質壓縮。 如需 Windows 媒體編解碼器的詳細資訊，請參閱[編解碼器功能](codec-features.md)。 許多其他編解碼器都可以從各種來源取得。 您可以在建立 ASF 檔案時使用您喜歡的任何編解碼器，但此 SDK 的物件只會直接支援 Windows 媒體編解碼器。 若要使用其他編解碼器，您必須壓縮範例，並將它們以任意資料的形式傳遞至寫入器物件。

音訊或影片串流與任意串流之間最重要的差別在於，包含 Windows 媒體音訊或影片資料的串流，會由 Windows 媒體格式 SDK 的物件進行驗證。 任意的資料流程都不會自動驗證，而且應該檢查您的應用程式是否有完整性。

音訊或影片資料流程的屬性會在用來建立檔案的設定檔中說明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**任意資料流程**](arbitrary-streams.md)
</dt> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 




