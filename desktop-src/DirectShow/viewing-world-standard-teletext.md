---
description: 觀賞全球標準 Teletext
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: 觀賞全球標準 Teletext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2129538d91a7ac48fea26fd5f1987473896760c164fb3e2b1d4a2b1d142a1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078541"
---
# <a name="viewing-world-standard-teletext"></a>觀賞全球標準 Teletext

> [!Note]  
> 這種功能已從 Windows Vista 和更新版本的作業系統中移除。 它可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。

 

全球標準 Teletext (WST) 會以垂直空白間隔編碼， (VBI) 的類比電視信號。 預覽 teletext 的篩選圖形類似于用來查看隱藏式輔助字幕的圖形。 下圖說明此圖形。

![wst 預覽圖形](images/vidcap10.png)

此圖表會使用下列篩選器來顯示 WST：

-   [T/接收到接收的轉換器](tee-sink-to-sink-converter.md)。 接受 capture 篩選器中的 VBI 資訊，並將其分割為信號上的每個資料服務的個別資料流程。
-   [WST 編解碼器](wst-codec-filter.md)。 解碼 VBI 範例中的 Teletext 資料。
-   [WST 解碼器](wst-decoder-filter.md)。 轉譯 teletext 的資料，並將文字繪製到點陣圖上。 下游篩選 (在此案例中，重迭 Mixer) 將點陣圖重迭到影片。

Capture Graph Builder 的 **RenderStream** 方法不會直接支援 WST 篩選，因此您的應用程式必須執行一些額外的工作。

1.  將覆迭 Mixer 篩選新增至篩選圖形。 下列程式碼會使用 [依 CLSID 加入篩選器](add-a-filter-by-clsid.md)中所述的 AddFilterByCLSID 函數。  (AddFilterByCLSID 不是 DirectShow API。 ) 
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  透過重迭 Mixer 連線預覽釘選到影片轉譯器篩選器。 您可以使用 **RenderStream** 方法，如下所示：
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  將端對端/接收到接收轉換器篩選加入至篩選圖形。 下列程式碼使用 [建立 Kernel-Mode 篩選準則](creating-kernel-mode-filters.md)中所述的 CreateKernelFilter 函數。  (CreateKernelFilter 不是 DirectShow API。 ) 
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  將 WST 編解碼器篩選器新增至篩選圖形：
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  呼叫 **RenderStream** 以將捕獲篩選器的 VBI 釘選到「t/接收」和「接收端對接收」轉換器，並將 T-sql 編解碼器篩選準則的 t/接收到接收轉換器：
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  再次呼叫 **RenderStream** ，以將 WST 編解碼器篩選器連線到重迭的 Mixer。 WST 解碼器篩選器會自動帶入圖形中。
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  請記得釋放所有篩選介面。
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> 目前，WST 解碼器篩選器不支援連接到 (VMR) 篩選器的視頻混合轉譯器。 因此，您必須使用舊版影片轉譯器篩選器來查看 teletext。

 

如果捕捉篩選器有影片埠 VBI pin (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI) ，請將它連線到 [VBI Surface](vbi-surface-allocator.md) 配置器篩選器。 否則，圖形將無法正確執行。 The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).  (兩個函式都不是 DirectShow API。 ) 


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[隱藏式輔助字幕和 Teletext](closed-captions-and-teletext.md)
</dt> </dl>

 

 



