---
title: 指派輸出格式
description: 指派輸出格式
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK，指派輸出格式
- Advanced Systems Format (ASF) ，指派輸出格式
- ASF (Advanced 系統格式) ，指派輸出格式
- Advanced Systems Format (ASF) 、output 數位和格式
- ASF (Advanced Systems Format) 、output 數位和格式
- 輸出編號和格式，指派
- 編解碼器、輸出編號和格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106968484"
---
# <a name="assigning-output-formats"></a>指派輸出格式

某些編解碼器可將數位媒體資料解壓縮成數個未壓縮的格式。 您可以使用非同步讀取器或同步讀取器，來尋找特定輸出的所有支援格式。

若要檢查輸出的所有可用格式，請執行下列步驟。 非同步讀取器和同步讀取器的這些程式都相同。 在介面名稱不同的情況下，同步讀取器方法會在非同步讀取器方法之後的括弧中列出。

1.  建立讀取器物件，並載入要讀取的檔案。 如需詳細資訊，請參閱 [建立讀取器和開啟](to-create-a-reader-and-open-a-file.md) 檔案 (或 [建立同步讀取器，並開啟](to-create-a-synchronous-reader-and-open-a-file.md) 檔案) 。
2.  判斷您想要尋找其可用格式的輸出。 如果您還不知道要使用哪一個輸出，可以使用中的程式識別 [輸出編號](to-identify-output-numbers.md)，以識別檔案中的輸出。
3.  藉由呼叫 [**IWMReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (或 [**IWMSyncReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)) ，來取得所需輸出的可用格式總數。
4.  逐一執行一次可用的格式，對每個格式執行下列步驟：
    -   藉由呼叫 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (或 [**IWMSyncReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)) ，取得目前輸出格式的 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)介面。
    -   藉由對 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)進行兩個呼叫，以取出輸出格式的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。 進行第一次呼叫以取得結構的大小，然後為其配置記憶體，並在第二次呼叫時將指標傳遞至配置的記憶體。
    -   在 **WM \_ 媒體 \_ 類型** 中尋找輸出格式的媒體子類型。子類型。
    -   針對影片，如果目前的子類型是您想要用於輸出的格式，請中斷迴圈。 否則，請移至下一個反復專案。

        若是音訊，您必須根據您的需求來檢查 **WAVEFORMATEX** 結構中的值。 **WM \_媒體 \_ 類型。 pbFormat** 指向音訊輸出的 **WAVEFORMATEX** 結構。

5.  當您找到所需的輸出時，請呼叫 [**IWMReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (或 [**IWMSyncReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)) 來設定它以搭配讀取器使用。 您必須將指標傳遞至在迴圈的第一個步驟中取得的 **IWMOutputMediaProps** 介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMMediaProps 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMOutputMediaProps 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**使用輸出**](working-with-outputs.md)
</dt> </dl>

 

 




