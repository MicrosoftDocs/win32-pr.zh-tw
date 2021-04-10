---
title: '設定 WM ASF 寫入器 (QASF) '
description: '設定 WM ASF 寫入器 (QASF) '
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- 'Windows Media 格式 SDK，設定 WM ASF 寫入器 (QASF) '
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，WM ASF 寫入器
- Windows Media Format SDK、QASF
- 'Advanced Systems Format (ASF) 、設定 WM ASF 寫入器 (QASF) '
- 'ASF (Advanced Systems Format) 、設定 WM ASF 寫入器 (QASF) '
- Advanced Systems Format (ASF) 、WM ASF 寫入器
- ASF (Advanced Systems Format) ，WM ASF 寫入器
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- 'DirectShow，設定 WM ASF 寫入器 (QASF) '
- DirectShow、WM ASF 寫入器
- DirectShow、QASF
- WM ASF 寫入器，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093107"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>設定 WM ASF 寫入器 (QASF) 

當您建立了 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器時，它會自動使用 WMProfile \_ V80 \_ 256Video 設定檔來設定為預設值。 因為此設定檔使用 Windows Media 音訊和 Windows Media 視訊第8版編解碼器，建議您建立使用 Windows Media 9 系列編解碼器的自訂設定檔，然後使用 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md)方法將其 [**IWMProfile**](iwmprofile.md)指標傳遞至篩選。 必須先將篩選新增至圖形，才能設定篩選，而且必須先設定篩選器，才能連接到上游篩選器。 此篩選器會使用設定檔來決定要寫入的 Windows Media 格式檔案類型、要設定的輸入釘選數目，以及 pin 可以接受的媒體類型。

當新的設定檔不需要任何額外的輸入 pin 時，篩選器可讓設定檔在其輸入 pin 連線時重設。 例如，如果您將設定檔從單一輸入的僅限音訊設定檔變更為雙輸入音訊和影片設定檔，則只需要將音訊 pin reconnectedAll 輸入資料必須加上時間戳記，而且必須先連接所有輸入圖釘，才能執行或暫停篩選。 這表示，如果您使用具有音訊串流和影片串流的設定檔來設定篩選準則，則篩選準則會建立音訊和影片輸入的 pin，而且必須先連接這兩個 pin，然後才能執行篩選。

新增資料單位延伸模組

您可以設定資料單位延伸模組的設定檔串流，例如在連接篩選器之前或之後的 SMPTE 時間代碼，只要遵循此作業順序：

1.  使用 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)，將一個或多個資料單位延伸加入至資料流程。
2.  呼叫 [**WMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) 來更新設定檔。
3.  以更新的設定檔物件呼叫 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) 。
4.  尋找影片輸入 pin，並呼叫其 [**IAMWMBufferPass：： SetNotify**](iamwmbufferpass-setnotify.md) 方法來註冊您的應用程式定義 [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) 介面。

當圖形執行時，將會針對每個框架呼叫 [**IAMWMBufferPassCallback：： Notify**](iamwmbufferpasscallback-notify.md) 方法，而且您將可以使用其 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) 介面方法來取得和設定範例上的屬性。

> [!Note]  
> 在某些耗用大量處理器的案例中，例如反向電視的情況下，WM ASF 寫入器可能需要的輸出緩衝區比某些下游篩選器可支援的更多。 例如，DV 解碼器將不會接受一個以上的緩衝區作為輸出 pin，而且在某些情況下，AVI 解壓縮程式也是如此。 如果您在嘗試連線至這些篩選器時遇到問題，或在執行圖形時遇到問題，可能需要撰寫可接受其輸出 pin 上任意數目緩衝區的中繼篩選。

 

 

 