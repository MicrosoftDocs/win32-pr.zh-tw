---
title: 撰寫壓縮的範例
description: 撰寫壓縮的範例
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Advanced Systems Format (ASF) 、撰寫壓縮的範例
- ASF (Advanced Systems Format) 、撰寫壓縮的範例
- Advanced Systems Format (ASF) ，傳遞壓縮的範例
- ASF (Advanced Systems Format) ，傳遞壓縮的範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104462712"
---
# <a name="writing-compressed-samples"></a>撰寫壓縮的範例

針對某些音訊或影片串流，您可能會想要傳遞已壓縮的範例，而不是傳遞原始資料。 這項功能是用來複製現有的資料流程，或是撰寫使用協力廠商編解碼器壓縮的範例。 撰寫壓縮範例的程式與寫入未壓縮的範例相同，不同之處在于您使用 [**IWMWriterAdvanced：： WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) 而不是 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)。 如需有關撰寫未壓縮範例的詳細資訊，請參閱 [撰寫範例](to-write-samples.md)。

當您針對 CBR 設定檔撰寫壓縮的範例時，寫入器會視需要卸載一些範例，以將內容保留在指定的位元速率和緩衝區視窗值內。 針對 VBR，寫入器不會捨棄範例，但無法確定位元速率和緩衝區視窗值是否正確。

如果您要將資料流程從某個檔案複製到另一個檔案，您應該一律將串流設定物件從原始檔案的配置檔案複製到新檔案的設定檔。 這可確保您擁有正確的位元速率和緩衝區視窗資訊。 如果您將壓縮的資料流程複製到已設定較低緩衝區視窗的資料流程，則會在檔案寫入期間卸載範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




