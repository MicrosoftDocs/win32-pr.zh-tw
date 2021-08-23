---
title: 任意和 Precompressed 的資料流程輸入
description: 任意和 Precompressed 的資料流程輸入
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF) 、任意資料流程輸入
- ASF (Advanced Systems Format) ，任意資料流程輸入
- 設定檔，任意資料流程輸入
- 編解碼器，任意資料流程輸入
- Advanced Systems Format (ASF) 、precompressed 資料流程輸入
- ASF (Advanced 系統格式) 、precompressed 資料流程輸入
- 設定檔，precompressed 資料流程輸入
- 編解碼器，precompressed 資料流程輸入
- precompressed 資料流程輸入
- 任意資料流程輸入
- 資料流程，任意資料流程輸入
- 資料流程，precompressed 資料流程輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0129362e8dc01b7ccf3faabbf10e22ffd4eccc082782796059b3cf4578c33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448268"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>任意和 Precompressed 的資料流程輸入

只有一個 Windows 媒體編解碼器所壓縮的輸入有多個可能的輸入。 其他類型的可能輸入為任意輸入和 precompressed 輸入。 本節將說明這些類型之輸入格式的需求。

## <a name="arbitrary-stream-inputs"></a>任意資料流程輸入

任意資料流程類型的輸入與設定檔中所述的資料流程格式相同。 您不應該設定這些類型的輸入格式。

## <a name="precompressed-stream-inputs"></a>Precompressed 資料流程輸入

將資料流程從某個檔案複製到另一個檔案時，您會傳遞已壓縮的範例。 在此情況下，您必須將 [輸入屬性] 物件設定為 **Null** ，以通知寫入器不需要驗證您要傳入的資料。 若要將輸入格式設定為 **Null**，請呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) ，並傳遞 **Null** 做為第二個參數。 使用 **Null** 參數呼叫這個方法時，您必須在呼叫 [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)之前進行呼叫。

使用 precompressed 串流時，您必須在寫入之前，手動將編解碼器資訊複製到檔案標頭。 若要取得編解碼器資訊，請呼叫 [**IWMHeaderInfo2：： GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) 和 [**IWMHeaderInfo2：： GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) ，以列舉讀取器中與檔案相關聯的編解碼器。 選取符合 precompressed 資料流程之資料流程設定的編解碼器資訊。 然後藉由呼叫 [**IWMHeaderInfo3：： AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)來設定寫入器中的編解碼器資訊，傳遞從讀取器取得的資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用輸入**](working-with-inputs.md)
</dt> </dl>

 

 




