---
description: 說明如何變更數學輸入控制項的外觀。
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: 自訂數學輸入控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3cab7c6efe003738c46a89d07866fcc9302ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555061"
---
# <a name="customizing-the-math-input-control"></a><span data-ttu-id="6259b-103">自訂數學輸入控制項</span><span class="sxs-lookup"><span data-stu-id="6259b-103">Customizing the Math Input Control</span></span>

<span data-ttu-id="6259b-104">您可以變更數學輸入控制項的外觀和風格，使其更適合您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6259b-104">It is possible to change the look and feel of the math input control so that it is better suited to your application.</span></span> <span data-ttu-id="6259b-105">本主題說明開發人員可以自訂數學輸入控制項的各種方式。</span><span class="sxs-lookup"><span data-stu-id="6259b-105">This topic explains the various ways that developers can customize the math input control.</span></span>

<span data-ttu-id="6259b-106">可能的自訂如下：</span><span class="sxs-lookup"><span data-stu-id="6259b-106">The following customizations are possible:</span></span>

-   [<span data-ttu-id="6259b-107">變更顯示的按鈕</span><span class="sxs-lookup"><span data-stu-id="6259b-107">Changing the Displayed Buttons</span></span>](#changing-the-displayed-buttons)
-   [<span data-ttu-id="6259b-108">變更控制項標題</span><span class="sxs-lookup"><span data-stu-id="6259b-108">Changing the Control Caption</span></span>](#changing-the-control-caption)
-   [<span data-ttu-id="6259b-109">變更控制項的預覽區域大小</span><span class="sxs-lookup"><span data-stu-id="6259b-109">Changing the Control's Preview Area Size</span></span>](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a><span data-ttu-id="6259b-110">變更顯示的按鈕</span><span class="sxs-lookup"><span data-stu-id="6259b-110">Changing the Displayed Buttons</span></span>

<span data-ttu-id="6259b-111">您可以變更數學輸入控制項上顯示的按鈕，讓控制項有擴充的功能，或在螢幕上顯示為較小。</span><span class="sxs-lookup"><span data-stu-id="6259b-111">You can change the buttons that are displayed on the math input control so that the control has extended functionality or appears smaller on the screen.</span></span> <span data-ttu-id="6259b-112">啟用擴充按鈕集將會顯示 [ **重做** ] 和 [ **復原** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6259b-112">Enabling the extended button set will show the **Redo** and **Undo** buttons.</span></span> <span data-ttu-id="6259b-113">下列程式碼顯示如何啟用擴充按鈕集。</span><span class="sxs-lookup"><span data-stu-id="6259b-113">The following code shows how to enable the extended button set.</span></span>


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



<span data-ttu-id="6259b-114">下圖顯示具有一組擴充按鈕的控制項。</span><span class="sxs-lookup"><span data-stu-id="6259b-114">The following image shows the control with the extended set of buttons.</span></span>

![具有一組擴充按鈕的數學輸入控制項](images/mic.png)

<span data-ttu-id="6259b-116">下圖顯示沒有一組擴充按鈕的控制項。</span><span class="sxs-lookup"><span data-stu-id="6259b-116">The following image shows the control without the extended set of buttons.</span></span>

![沒有一組擴充按鈕的數學輸入控制項](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a><span data-ttu-id="6259b-118">變更控制項標題</span><span class="sxs-lookup"><span data-stu-id="6259b-118">Changing the Control Caption</span></span>

<span data-ttu-id="6259b-119">您可以變更數學輸入控制項的控制項標題，以便在數學輸入控制項的視窗上設定標題。</span><span class="sxs-lookup"><span data-stu-id="6259b-119">You can change the control caption for the math input control in order to set the caption on the math input control's window.</span></span> <span data-ttu-id="6259b-120">下列程式碼顯示如何設定標題。</span><span class="sxs-lookup"><span data-stu-id="6259b-120">The following code shows how to set the caption.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



<span data-ttu-id="6259b-121">下圖顯示在設定標題之後的控制項。</span><span class="sxs-lookup"><span data-stu-id="6259b-121">The following image shows the control after the caption has been set.</span></span>

![具有標題集的數學輸入控制項](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a><span data-ttu-id="6259b-123">變更控制項的預覽區域大小</span><span class="sxs-lookup"><span data-stu-id="6259b-123">Changing the Control's Preview Area Size</span></span>

<span data-ttu-id="6259b-124">您可以自訂數學輸入控制項，讓控制項明確地設定其預覽區域的大小。</span><span class="sxs-lookup"><span data-stu-id="6259b-124">You can customize the math input control so that the control explicitly sets its preview-area size.</span></span> <span data-ttu-id="6259b-125">這會建立一個較大的區域，其中會顯示數學公式。</span><span class="sxs-lookup"><span data-stu-id="6259b-125">This creates a larger area in which the math formulas are displayed.</span></span> <span data-ttu-id="6259b-126">下列程式碼顯示如何設定預覽區域大小。</span><span class="sxs-lookup"><span data-stu-id="6259b-126">The following code shows how to set the preview area size.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



<span data-ttu-id="6259b-127">下列影像顯示的控制項具有不同大小的預覽區域。</span><span class="sxs-lookup"><span data-stu-id="6259b-127">The following images show a control with differently sized preview areas.</span></span>

![具有預設預覽區域大小的數學輸入控制項](images/mic.png)![具有較大預覽區域的數學輸入控制項](images/mic-big-preview.png)

 

 



