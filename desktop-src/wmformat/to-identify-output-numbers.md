---
title: 識別輸出編號
description: 識別輸出編號
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows媒體格式 SDK，識別輸出編號
- Advanced Systems Format (ASF) ，識別輸出編號
- ASF (Advanced 系統格式) ，識別輸出編號
- Advanced Systems Format (ASF) 、output 數位和格式
- ASF (Advanced Systems Format) 、output 數位和格式
- 輸出編號和格式，識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c601481520632806ac56e12e16e1474336897d1be341c9d19df8e235d6355ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699378"
---
# <a name="to-identify-output-numbers"></a>識別輸出編號

若要識別已載入檔案的輸出編號，請執行下列步驟。 非同步讀取器和同步讀取器的這些程式都相同。 在介面名稱不同的情況下，同步讀取器方法會在非同步讀取器方法之後的括弧中列出。

1.  建立讀取器物件，並載入要讀取的檔案。 如需詳細資訊，請參閱 [建立讀取器和開啟](to-create-a-reader-and-open-a-file.md) 檔案 (或 [建立同步讀取器，並開啟](to-create-a-synchronous-reader-and-open-a-file.md) 檔案) 。
2.  藉由呼叫 [**IWMReader：： GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (或 [**IWMSyncReader：： GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)) ，來取出檔案的輸出總數。
3.  逐一執行一次輸出，執行下列步驟：
    -   使用 [**IWMReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (或 [**IWMSyncReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)) 的呼叫，以取得目前輸出的 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)介面。
    -   對 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)進行兩次呼叫，以抓取輸出的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。 進行第一次呼叫以取得結構的大小，然後為其配置記憶體，並在第二次呼叫時將指標傳遞至配置的記憶體。 或者，您可以呼叫 [**IWMMediaProps：： GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype)以傳遞主要型別，而不需要為 **WM \_ 媒體 \_ 類型** 結構配置記憶體。 您可以略過錯誤主要類型的輸出。
    -   從 **WM \_ 媒體 \_ 類型** 結構取出主要媒體類型和媒體子類型。 這些值分別儲存在資料成員 **majortype** 和 **子類型** 中。
    -   檢查 **WM \_ 媒體 \_ 類型** 的值 formattype。 這會指定以 **WM \_ 媒體 \_ 類型 pbFormat** 之緩衝區中包含的結構類型。 如需有關格式類型的詳細資訊，請參閱 [媒體類型](media-types.md)。
    -   配置記憶體來保存上一個步驟中所識別之類型的結構。 將結構複製到配置的記憶體。 針對音訊和影片，此結構提供有關如何呈現資料的重要資訊。

同步讀取器也會提供方法，以取得輸出數位與資料流程號碼之間的關聯。 如需詳細資訊，請參閱 [尋找資料流程號碼和輸出編號](to-find-stream-numbers-and-output-numbers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> <dt>

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

 

 




