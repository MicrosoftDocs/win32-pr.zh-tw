---
title: 設定檔案傳輸資料流程
description: 設定檔案傳輸資料流程
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- 資料流程，設定檔案傳輸資料流程
- 編解碼器，設定檔案傳輸串流
- 檔案傳輸資料流程
- 資料流程，資料單位延伸
- 編解碼器，資料單位延伸
- 資料單位延伸模組，檔案傳輸資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023079"
---
# <a name="configuring-file-transfer-streams"></a>設定檔案傳輸資料流程

在 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構中，檔案傳輸資料流程不需要任何特殊設定。 它們需要資料單位延伸模組，才能將檔案名與每個範例產生關聯。 若要使用檔案傳輸範例來傳送名稱，您必須為數據流執行資料單位延伸系統。

若要設定資料流程的資料單位延伸，請執行下列步驟：

1.  藉由呼叫 **IWMStreamConfig：： QueryInterface**，取得資料流程設定物件之 [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)介面的指標。
2.  藉由呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 來新增資料流程的資料單位延伸，如下所示：
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定任意資料流程類型**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**檔案資料流程**](file-streams.md)
</dt> </dl>

 

 




