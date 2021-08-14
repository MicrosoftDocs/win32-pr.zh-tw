---
description: 說明如何變更數學輸入控制項的外觀。
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: 自訂數學輸入控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adedc4ab5b655f4f753a1b83cabe28e322adaad3c73bcf9f25ea1dea6d0bc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045621"
---
# <a name="customizing-the-math-input-control"></a>自訂數學輸入控制項

您可以變更數學輸入控制項的外觀和風格，使其更適合您的應用程式。 本主題說明開發人員可以自訂數學輸入控制項的各種方式。

可能的自訂如下：

-   [變更顯示的按鈕](#changing-the-displayed-buttons)
-   [變更控制項標題](#changing-the-control-caption)
-   [變更控制項的預覽區域大小](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>變更顯示的按鈕

您可以變更數學輸入控制項上顯示的按鈕，讓控制項有擴充的功能，或在螢幕上顯示為較小。 啟用擴充按鈕集將會顯示 [ **重做** ] 和 [ **復原** ] 按鈕。 下列程式碼顯示如何啟用擴充按鈕集。


```
  void CMath_Input_Control_testDlg::OnBnClickedToggleBtns()
  {
    static bool enabled = true;
    HRESULT hr = S_OK;

    hr = g_spMIC->Hide();    
    if(!enabled){
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
        enabled = true;
      }
    }else{
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_FALSE);
        enabled = false;
      }
    }
    if (SUCCEEDED(hr)){
      hr = g_spMIC->Show();
    }
  }
  
```



下圖顯示具有一組擴充按鈕的控制項。

![具有一組擴充按鈕的數學輸入控制項](images/mic.png)

下圖顯示沒有一組擴充按鈕的控制項。

![沒有一組擴充按鈕的數學輸入控制項](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>變更控制項標題

您可以變更數學輸入控制項的控制項標題，以便在數學輸入控制項的視窗上設定標題。 下列程式碼顯示如何設定標題。


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



下圖顯示在設定標題之後的控制項。

![具有標題集的數學輸入控制項](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>變更控制項的預覽區域大小

您可以自訂數學輸入控制項，讓控制項明確地設定其預覽區域的大小。 這會建立一個較大的區域，其中會顯示數學公式。 下列程式碼顯示如何設定預覽區域大小。


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



下列影像顯示的控制項具有不同大小的預覽區域。

![具有預設預覽區域大小的數學輸入控制項](images/mic.png)![具有較大預覽區域的數學輸入控制項](images/mic-big-preview.png)

 

 



