---
description: 顯示 VFW 捕捉對話方塊
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: 顯示 VFW 捕捉對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687503"
---
# <a name="display-vfw-capture-dialog-boxes"></a>顯示 VFW 捕捉對話方塊

仍使用 Windows (VFW) 驅動程式影片的捕獲裝置可支援下列任何三個對話方塊，可用來設定裝置。



| 對話方塊    | 描述                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| 影片來源  | 用來選取影片輸入，以及調整裝置設定，例如圖片亮度或對比。 |
| 影片格式  | 用來選取影像維度和位深度。                                                    |
| 影片顯示 | 用來控制呈現影片的外觀。                                                 |



 

若要顯示這些對話方塊的其中一個，請執行下列動作：

1.  停止篩選圖形。
2.  查詢 [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) 介面的 capture 篩選器。 如果 **QueryInterface** 成功，則表示 capture 裝置為 VFW 裝置。
3.  呼叫 [**IAMVfwCaptureDialogs：： HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) ，以檢查驅動程式是否支援您想要顯示的對話方塊。 [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs)列舉會定義每個 VFW 對話方塊的旗標。 如果支援此對話方塊， **HasDialog** 會傳回 S \_ OK。 否則，它會傳回 \_ FALSE，因此請直接檢查值 s \_ OK，而不是使用 **SUCCEEDED** 宏。
4.  如果支援對話方塊，請呼叫 [**IAMVfwCaptureDialogs：： ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) 來顯示對話方塊。
5.  重新開機圖形。

下列程式碼顯示 [影片來源] 對話方塊的下列步驟：


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定影片捕獲裝置](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



