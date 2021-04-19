---
description: 當應用程式視窗處於作用中狀態，且處於全螢幕模式 (或擁有的視窗為使用中時，防止 edge 手勢的行為) 。
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: EdgeGesture. DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996954"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a><span data-ttu-id="d2cc0-103">EdgeGesture. DisableTouchWhenFullscreen</span><span class="sxs-lookup"><span data-stu-id="d2cc0-103">System.EdgeGesture.DisableTouchWhenFullscreen</span></span>

<span data-ttu-id="d2cc0-104">當應用程式視窗處於作用中狀態，且處於全螢幕模式 (或擁有的視窗為使用中時，防止 edge 手勢的行為) 。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-104">Prevents edge gesture behaviors when an application window is active and in full-screen mode (or an owned window is active).</span></span>

> [!Note]  
> <span data-ttu-id="d2cc0-105">在全螢幕模式中，應用程式視窗的大小與螢幕解析度相符。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-105">In full-screen mode, the size of the application window matches the screen resolution.</span></span>

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="d2cc0-106">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8</span><span class="sxs-lookup"><span data-stu-id="d2cc0-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="d2cc0-107">備註</span><span class="sxs-lookup"><span data-stu-id="d2cc0-107">Remarks</span></span>

<span data-ttu-id="d2cc0-108">在 Windows 8 中，與畫面邊緣互動的使用者會顯示系統 UI，例如應用程式橫條、常用鍵和執行中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-108">In Windows 8, user interactions with the edges of the screen display system UI such as app bars, charms, and running apps.</span></span>

<span data-ttu-id="d2cc0-109">針對全螢幕的遠端應用程式，本機電腦上的這個 UI 行為可能會覆寫並干擾遠端會話的 UI。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-109">For full-screen, remote applications, this UI behavior on the local machine might override and interfere with the UI of the remote session.</span></span> <span data-ttu-id="d2cc0-110">這個屬性可讓應用程式停用本機電腦上的 edge UI。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-110">This property enables an application to disable the edge UI on the local machine.</span></span>

<span data-ttu-id="d2cc0-111">若要停用 edge UI，請將此屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-111">To disable edge UI, set this property to VARIANT\_TRUE.</span></span> <span data-ttu-id="d2cc0-112">預設值為 VARIANT \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-112">The default value is VARIANT\_FALSE.</span></span>

<span data-ttu-id="d2cc0-113">這個屬性不會影響 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-113">This property has no effect on Windows Store apps.</span></span>

<span data-ttu-id="d2cc0-114">下列範例顯示如何設定 edge UI 行為。</span><span class="sxs-lookup"><span data-stu-id="d2cc0-114">The following example shows how to set edge UI behaviors.</span></span>


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a><span data-ttu-id="d2cc0-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2cc0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2cc0-116">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d2cc0-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d2cc0-117">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d2cc0-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d2cc0-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d2cc0-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
