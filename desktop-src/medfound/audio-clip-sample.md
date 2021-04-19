---
description: 示範如何使用 Microsoft 媒體基礎將音訊從媒體檔案解碼。
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: 音訊剪輯範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972155"
---
# <a name="audio-clip-sample"></a>音訊剪輯範例

示範如何使用 Microsoft 媒體基礎將音訊從媒體檔案解碼。

音訊剪輯範例應用程式會從媒體檔案讀取音訊資料，並將未壓縮的音訊寫入 WAVE 檔。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>使用方式

此範例是命令列應用程式。 它會使用下列命令列引數：

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   inputfile：包含音訊資料流程的檔案名。
-   outputfile .wav：要寫入的 WAVE 檔案名稱。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> <dt>

[教學課程：解碼音訊](tutorial--decoding-audio.md)
</dt> </dl>

 

 



