---
title: Windows 精確度的觸控板裝置
description: Windows 精確度的觸控板裝置
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb81978c9c9849dfa0d073a4b37af3760d1d4e5bc8e8fa2e81317293db04fc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007898"
---
# <a name="windows-precision-touchpad-devices"></a>Windows 精確度的觸控板裝置

## <a name="platforms"></a>平台

<dl> 用戶端-Windows 8。1  
</dl>

## <a name="description"></a>描述

Windows 精確度觸控板是新的輸入裝置類別，可提供高精確度的指標輸入和手勢功能。 根據預設，這些裝置會產生超高精確度的滾動滾輪訊息，以供桌面應用程式取用。

## <a name="manifestations"></a>表現

設計用來處理超高精確度滾輪訊息的應用程式，可能會無法正確地滾動。

## <a name="mitigation"></a>降低

應用程式開發人員應該查看滑鼠滾輪訊息中的滾動差異，並據以修改其應用程式;不過，在過渡期間，應用程式可能會退出宣告超高精確度的滾動滾輪訊息 (delta = 1) 然後選擇接收高精確度的滾輪訊息 (delta = 40) 或標準滾動滾輪訊息 (delta = 120) 。

## <a name="solution"></a>解決方案

如果應用程式能夠處理超高精確度的滾輪訊息，則不需要執行任何動作，因為這是 Windows 精確度 Touchpads 所傳送的預設訊息。

如果應用程式能夠處理高精確度的滾輪訊息，但不能處理超高精確度的滾輪訊息，請將下列內容新增至應用程式資訊清單：


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



如果應用程式無法處理高精確度滾輪訊息或超高精確度滾輪訊息，請將下列內容新增至應用程式資訊清單，以指出需要標準滾動滾輪訊息：


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




