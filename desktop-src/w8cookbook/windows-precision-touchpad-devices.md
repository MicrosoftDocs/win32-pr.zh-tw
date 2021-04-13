---
title: Windows 精確的觸控板裝置
description: Windows 精確的觸控板裝置
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "104374170"
---
# <a name="windows-precision-touchpad-devices"></a><span data-ttu-id="1dff7-103">Windows 精確的觸控板裝置</span><span class="sxs-lookup"><span data-stu-id="1dff7-103">Windows precision touchpad devices</span></span>

## <a name="platforms"></a><span data-ttu-id="1dff7-104">平台</span><span class="sxs-lookup"><span data-stu-id="1dff7-104">Platforms</span></span>

<dl> <span data-ttu-id="1dff7-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="1dff7-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="1dff7-106">Description</span><span class="sxs-lookup"><span data-stu-id="1dff7-106">Description</span></span>

<span data-ttu-id="1dff7-107">Windows 有效位數觸控板是新的輸入裝置類別，可提供高精確度的指標輸入和手勢功能。</span><span class="sxs-lookup"><span data-stu-id="1dff7-107">The Windows Precision Touchpad is a new class of input devices that provide high precision pointer input and gesture functionality.</span></span> <span data-ttu-id="1dff7-108">根據預設，這些裝置會產生超高精確度的滾動滾輪訊息，以供桌面應用程式取用。</span><span class="sxs-lookup"><span data-stu-id="1dff7-108">By default, these devices generate ultra-high precision scroll wheel messages for desktop application consumption.</span></span>

## <a name="manifestations"></a><span data-ttu-id="1dff7-109">表現</span><span class="sxs-lookup"><span data-stu-id="1dff7-109">Manifestations</span></span>

<span data-ttu-id="1dff7-110">設計用來處理超高精確度滾輪訊息的應用程式，可能會無法正確地滾動。</span><span class="sxs-lookup"><span data-stu-id="1dff7-110">Applications that are not designed to handle ultra-high precision scroll wheel messages may either over-scroll or not scroll correctly.</span></span>

## <a name="mitigation"></a><span data-ttu-id="1dff7-111">降低</span><span class="sxs-lookup"><span data-stu-id="1dff7-111">Mitigation</span></span>

<span data-ttu-id="1dff7-112">應用程式開發人員應該查看滑鼠滾輪訊息中的滾動差異，並據以修改其應用程式;不過，在過渡期間，應用程式可能會退出宣告超高精確度的滾動滾輪訊息 (delta = 1) 然後選擇接收高精確度的滾輪訊息 (delta = 40) 或標準滾動滾輪訊息 (delta = 120) 。</span><span class="sxs-lookup"><span data-stu-id="1dff7-112">Application developers should look at the scroll delta in mouse scroll wheel messages and modify their apps accordingly; however, in the interim an application may opt-out of ultra-high precision scroll wheel messages (delta = 1)and elect to receive high precision scroll wheel messages (delta = 40) or standard scroll wheel messages (delta = 120).</span></span>

## <a name="solution"></a><span data-ttu-id="1dff7-113">解決方法</span><span class="sxs-lookup"><span data-stu-id="1dff7-113">Solution</span></span>

<span data-ttu-id="1dff7-114">如果應用程式能夠處理超高精確度的滾輪訊息，則不需要執行任何動作，因為這是 Windows Precision Touchpads 所傳送的預設訊息。</span><span class="sxs-lookup"><span data-stu-id="1dff7-114">If the application is capable of handling ultra-high precision scroll wheel messages, nothing needs to be done as this is the default message sent by Windows Precision Touchpads.</span></span>

<span data-ttu-id="1dff7-115">如果應用程式能夠處理高精確度的滾輪訊息，但不能處理超高精確度的滾輪訊息，請將下列內容新增至應用程式資訊清單：</span><span class="sxs-lookup"><span data-stu-id="1dff7-115">If the application is capable of handling high precision scroll wheel messages, but not ultra-high precision wheel messages, add the following to the application manifest:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



<span data-ttu-id="1dff7-116">如果應用程式無法處理高精確度滾輪訊息或超高精確度滾輪訊息，請將下列內容新增至應用程式資訊清單，以指出需要標準滾動滾輪訊息：</span><span class="sxs-lookup"><span data-stu-id="1dff7-116">If the application is not capable of handling either high precision scroll wheel messages or ultra-high precision wheel messages, add the following to the application manifest to indicate that standard scroll wheel messages are desired:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




