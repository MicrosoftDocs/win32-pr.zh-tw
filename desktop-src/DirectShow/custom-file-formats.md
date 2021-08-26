---
description: 自訂檔案格式
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: 自訂檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a478e7818701008c31d1d0c5a6e4924540ed818be19f7b50fe3ed278aa6f3ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998688"
---
# <a name="custom-file-formats"></a>自訂檔案格式

如果您有支援您自己的檔案格式的自訂 mux 或檔案寫入器篩選器，則可以指定 CLSID 作為 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法的第一個參數：


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



如需此用法的詳細資訊，請參閱 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將影片捕獲至檔案](capturing-video-to-a-file.md)
</dt> </dl>

 

 



