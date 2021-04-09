---
description: 本主題說明應用程式如何以程式設計方式變更影片捕獲裝置上的影像和相機設定。
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: 設定影片品質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687704"
---
# <a name="configure-the-video-quality"></a>設定影片品質

本主題說明應用程式如何以程式設計方式變更影片捕獲裝置上的影像和相機設定。

-   [ProcAmp 設定](#procamp-settings)
-   [照相機設定](#camera-settings)
-   [相關主題](#related-topics)

## <a name="procamp-settings"></a>ProcAmp 設定

Windows Driver Model (WDM) 視頻攝影機可以支援控制影像品質的屬性：

-   背光補償
-   亮度
-   這個
-   獲得
-   色差補正
-   色調
-   飽和度
-   清晰度
-   白平衡

這些屬性是透過 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) 介面來控制。 使用此介面，如下所示：

1.  在 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)介面的 capture 篩選器上呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。
2.  針對您想要設定的每個屬性，呼叫 [**IAMVideoProcAmp：： GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) 方法。 屬性是由 [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) 列舉所指定。 如果 **GetRange** 方法失敗，則表示相機不支援該特定屬性。
3.  如果 [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) 成功，它會傳回屬性的支援值範圍、預設值，以及最小增量。
4.  若要取得屬性目前的值，請呼叫 [**IAMVideoProcAmp：： get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get)。
5.  若要設定屬性，請呼叫 [**IAMVideoProcAmp：： set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) 方法。 若要將屬性還原為預設值，請呼叫 [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) 來尋找預設值，並將該值傳遞至 **Set** 方法。

當您設定屬性時，不需要停止篩選圖形。

下列程式碼會設定 [程式碼] 控制項，讓它可以用來設定亮度。 涵蓋範圍的範圍對應至裝置所支援的亮度範圍，而對應項的位置則對應于裝置的初始亮度設定。


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a>照相機設定

[**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)介面類別似于 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)，但會控制攝影機本身的各種不同的功能：

-   曝光
-   焦點
-   虹膜
-   移動瀏覽
-   Roll
-   傾斜
-   Zoom

若要使用此介面，請依照用於 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)的相同步驟執行：

1.  查詢 [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)的捕獲篩選。
2.  呼叫 [**IAMCameraControl：： GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) ，尋找支援的設定，以及每個設定的可能範圍。
3.  呼叫 [**IAMCameraControl：： get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) 以取得設定的目前值。
4.  呼叫 [**IAMCameraControl：： set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) 來設定值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定影片捕獲裝置](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
