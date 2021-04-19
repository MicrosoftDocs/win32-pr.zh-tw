---
description: 資料流程格式
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: 資料流程格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980602"
---
# <a name="stream-format"></a>資料流程格式

MSDV 和 UVC 驅動程式都可以輸出兩種 DV 格式：交錯音訊-影片或僅限影片。 交錯音訊-影片是來自裝置的原始格式。 僅限影片的格式包含相同的資料，但範例標示為沒有音訊資料。 僅限影片的格式存在，主要是為了與使用適用于 Windows 的影片的應用程式相容。 如需詳細資訊，請參閱 [type-1 與 type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md)。

**MSDV 驅動程式**

MSDV 驅動程式有兩個輸出圖釘。 第一個輸出圖釘會傳送交錯的資料，而第二個輸出圖釘會傳送僅限影片的資料。 一次只能連接一個輸出 pin。 若要選取格式，請連接適當的輸出 pin。 您可以在輸出釘選上使用 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面，以找出格式。

**UVC 驅動程式**

與 MSDV 驅動程式不同的是，UVC 驅動程式會從相同的 pin 提供這兩種格式。 預設格式為僅限影片。 若要選取格式，請在輸出釘選上使用 **IAMStreamConfig** 介面。 呼叫 **GetStreamCaps** 方法，以列舉輸出釘選上的媒體類型。 針對每個媒體類型，如果主要類型符合所需的格式，請呼叫 **SetFormat** 並傳入該媒體類型。



| 格式                      | 主要類型             |
|-----------------------------|------------------------|
| 交錯音訊和影片 | 媒體的 \_ 交錯 |
| 僅影片                  | 媒體 \_ 媒體       |



 

下列函式會根據主要型別 GUID 來設定格式。


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



MSDV 驅動程式也支援 **IAMStreamConfig**，因此您可以撰寫適用于這兩種裝置類型的程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



