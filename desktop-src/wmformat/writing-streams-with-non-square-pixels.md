---
title: 以非正方形圖元撰寫資料流程
description: 以非正方形圖元撰寫資料流程
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK，撰寫影片串流
- Windows Media Format SDK、影片串流
- Windows Media Format SDK、非正方形圖元
- 'Windows Media 格式 SDK，圖元 (非正方形) '
- Advanced Systems Format (ASF) 、撰寫影片串流
- ASF (Advanced 系統格式) 、撰寫影片串流
- Advanced Systems Format (ASF) 、影片串流
- ASF (Advanced 系統格式) 、影片串流
- Advanced Systems Format (ASF) 、非平方圖元
- ASF (Advanced Systems Format) 、非正方形圖元
- 'Advanced Systems Format (ASF) 、圖元 (非正方形) '
- 'ASF (Advanced Systems Format) ，圖元 (非正方形) '
- 撰寫影片串流
- 影片串流，書寫
- 影片串流，非正方形圖元
- 非正方形圖元
- '圖元 (非正方形) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023035"
---
# <a name="writing-streams-with-non-square-pixels"></a>以非正方形圖元撰寫資料流程

有兩種方式可以建立具有非正方形圖元的影片串流，以在 Windows Media Player 中正確顯示。 第一個技巧牽涉到在檔案標頭中設定資料流程層級的屬性。 第二個技術牽涉到將資料單位延伸加入至設定檔中的資料流程，然後在每個寫入的範例中設定其值。

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>若要使用資料流程層級的標頭屬性來設定圖元外觀比例

1.  設定寫入器物件。 如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。
2.  使用一或多個影片串流建立或載入設定檔。 如需詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。
3.  呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)。  (一律在設定任何標頭屬性之前呼叫這個方法。 ) 
4.  呼叫 **QueryInterface** 來取得 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面並呼叫 [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 兩次，以將 [**AspectRatioX**](aspectratiox.md) 和 [**AspectRatioY**](aspectratioy.md) 新增為影片資料流程的資料流程層級屬性。 這些屬性是 **DWORD** 值。
5.  寫入檔案。

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>使用資料單位延伸設定圖元外觀比例

**撰寫之前：**

1.  設定寫入器物件。 如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。
2.  使用一或多個影片串流建立或載入設定檔。 如需詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。
3.  針對) 在設定檔中任何媒體類型的每個資料流程 (，呼叫 [**IWMStreamConfig：： SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) 來指定您選擇的唯一名稱。 請勿提供兩個相同名稱的資料流程。
4.  使用影片串流上的 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 來新增圖元外觀比例的資料單位延伸。
5.  呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)。
6.  寫入檔案。

**撰寫時：**

-   針對每個範例，呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 並指定 WM \_ SampleExtensionGUID \_ PixelAspectRatio 屬性以及正確的值。 外觀比例值會以兩個串連的兩位數值寫入。 例如，16:9 是以1609或0x0649 撰寫。 這一律是2個位元組的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用非正方形圖元讀取和寫入影片串流**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




