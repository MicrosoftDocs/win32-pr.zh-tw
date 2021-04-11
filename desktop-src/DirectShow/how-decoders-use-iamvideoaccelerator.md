---
description: 解碼器如何使用 IAMVideoAccelerator
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: 解碼器如何使用 IAMVideoAccelerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436768b3561a999f6708ef4f6438b816e0ad303b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935623"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>解碼器如何使用 IAMVideoAccelerator

[**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)介面可啟用一般影片加速作業，包括 DirectX video 加速 (VA) 。 針對非 DirectX VA 加速，解碼器和 video 驅動程式必須遵守一般通訊協定。

本節說明使用這個介面時，任何解碼器應遵循的一般作業順序。 您可以在將 [Directx Video 加速對應至 IAMVideoAccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md)時，找到 directx VA 型解碼器特定的進一步資訊。

> [!Note]  
> 此介面可在 Windows 2000 和更新版本中使用。

 

[**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)介面會在重迭 [混音](overlay-mixer-filter.md)器的輸入 pin 或影片混合轉譯器 (VMR) 上公開。 [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify)介面會公開在解碼器的輸出圖釘上。 連接篩選器釘選的事件順序如下所示：

1.  篩選圖形管理員會在解碼篩選器的輸出釘選上呼叫 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 。 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)是選擇性參數。
    -   [**AM \_媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 是描述媒體類型的資料結構。 它包含 majortype GUID (在我們的案例中，應該是媒體 \_ 類型的影片) ，也就是在我們的案例中，它應該是影片加速器 guid) 和各種其他專案的型別 guid (。 其中一個專案是包含媒體相關資訊的格式類型 GUID，包括在我們的案例中，未壓縮影片的寬度和高度（最有可能在 [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)、 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)、 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構中）。
    -   [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構（如果有的話）會使用指定的媒體類型（可能是「完整指定」或「部分指定」）來指示解碼器運作。 如果是「完整指定」，則此解碼器通常只會嘗試使用該媒體類型來操作。 如果「部分指定」，則會嘗試找出「完全指定」相容的作業模式，它可以用來以與「部分指定」媒體類型一致的方式進行連接。
    -   嘗試尋找要用於連線之「完整指定」媒體類型的一般方式，是直接執行輸出釘選所支援的每一種「完整指定」媒體類型的清單，其與「部分指定的」媒體類型相容，並嘗試與每個媒體類型進行連接，直到成功為止。 如果 \_ \_ [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 呼叫中沒有包含媒體類型，但需要檢查其所有媒體類型的輸出 pin，則程式通常會類似。
2.  如果此解碼器想要檢查下游輸入 pin 是否支援特定的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) (包括影片加速器 guid) ，它可以使用影片加速器 guid 來呼叫該 pin 的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (，以作為 **AM \_ 媒體 \_ 類型** 的子類型) 或直接嘗試連接到該 pin，如下面的專案5所述。
3.  如果此解碼器不知道下游輸入 pin 所支援的影片加速器 Guid，而且不想要藉由呼叫下游輸入 pin 的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)來建議特定的候選影片加速器 guid，則此解碼器可以呼叫 [**IAMVideoAccelerator：： GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) 來取得 pin 所支援的影片加速器 guid 清單。
4.  針對某些特定的影片加速器 Guid，此解碼器可以呼叫下游輸入釘選的 [**IAMVideoAccelerator：： GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) ，以取得可用於轉譯特定影片加速器 GUID 的 **DDPIXELFORMAT** 像素格式清單。 傳回的清單應該被視為遞減喜好設定順序 (也就是最偏好的格式是第一個) 。
5.  此解碼器會呼叫下游輸入釘選的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)，並以適當的影片加速器 GUID 作為媒體類型的子類型，將它傳遞給它。 [**\_ \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) 這會設定作業的連線，包括建立未壓縮的輸出介面 (這些介面是使用「 **\_ 媒體 \_ 類型**」中的寬度和高度來配置，而您也可以透過下列方式的呼叫來配置要配置的介面數目，以及影片加速器可使用的任何其他資訊，例如影片加速器 GUID 本身) 。 如果下游輸入 pin 拒絕了影片加速器 GUID 或連線的其他某些層面，這可能會導致 **IPin：： ReceiveConnection** 失敗。 如果 **IPin：： ReceiveConnection** 失敗，則會在傳回的 **HRESULT** 中指出這一點，而且此解碼器可以嘗試再次呼叫，例如， **AM \_ 媒體 \_ 類型** 結構中有新的影片加速器 GUID。
    -   [!Note]  
        > 這是另一種方式 (以及最明確的方法) ，以判斷下游輸入 pin 所支援的內容，只要呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 並嘗試連接，然後檢查連接是否成功。

         

    -   在 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)期間，轉譯器會呼叫該解碼器的 [**IAMVideoAcceleratorNotify：： GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)，並將影片加速器 GUID 和 [**AMVAUncompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) 結構傳遞給它，以找出要配置多少未壓縮的表面。 此解碼器會填滿並傳回結構，其中包含要配置給特定類型的最小和最大介面數目，以及描述要配置之介面之像素格式的 **DDPIXELFORMAT** 結構。
    -   [!Note]  
        > 在 [**IAMVideoAcceleratorNotify：： GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) 的呼叫中，實際上不會將任何內容傳遞給解碼，而非影片加速器 GUID。

         

6.  轉譯器會呼叫 [**IAMVideoAcceleratorNotify：： SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)，並將已配置的未壓縮表面實際數目傳遞給該解碼器。
7.  轉譯器會呼叫解碼器的 [**IAMVideoAcceleratorNotify：： GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) ，以取得初始化影片加速器所需的任何資料。
8.  此解碼器會呼叫 [**IAMVideoAccelerator：： GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo)，並將影片加速器 GUID、 [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) 結構和壓縮的緩衝區類型數目傳遞給它，以傳回一組 [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) 資料結構，其中一個對應于影片加速器 GUID 所使用的每個壓縮資料緩衝區類型。
    -   [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo)結構包含已解碼之未壓縮資料的寬度和高度 (（以圖元為單位）) 和未壓縮圖片的 DDPIXELFORMAT。
    -   每個傳回的 [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) 資料結構都包含：
        -   特定類型所需的壓縮緩衝區數目。
        -   介面的寬度和高度，可建立 (欄位，而不一定會有任何真正的意義) 。
            > [!Note]  
            > 針對壓縮緩衝區的 DirectDraw 表面配置作業，目前不會將這些表面的寬度或高度提供為大於或等於 2 ^ 15，不過如果違反這項限制，表面配置呼叫可能不會 overtly 失敗。 因此，驅動程式可以為其壓縮緩衝區記憶體的要求設定結構，以避免這種極端的大小。 例如，而不是要求 width = "1" 和 height = "65536" 的緩衝區，驅動程式應該要求 width = "1024" 和 height = "64" 的緩衝區。

             

        -   介面要使用的總位元組數。
        -   **DDSCAPS2** 定義 DirectDrawSurface 物件之類型的結構，描述用來建立用來儲存壓縮資料之表面的功能。
        -   DDPIXELFORMAT，描述用來建立介面的像素格式，以將壓縮的資料儲存 (不一定具有任何實際意義) 的欄位。

> [!Note]  
> 轉譯器對某些解碼器 [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) 介面方法的呼叫可能 (，且通常會) 出現在對轉譯器的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)呼叫中。 具體而言，這適用于下列各項：
>
> -   [**IAMVideoAcceleratorNotify：： GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)、
> -   [**IAMVideoAcceleratorNotify：： SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)和
> -   [**IAMVideoAcceleratorNotify：： GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata)。

 

> [!Note]  
> 為了支援動態格式變更，在連接和執行篩選器時，解碼器也可能會呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 和上述的其他方法。 提供這項功能的目的是為了支援動態格式變更 (雖然不是在 .H、附錄 P、意義上，因為所有資料集都是從頭開始，而且任何參考圖片資訊都會遺失) 。

 

以下是在初始化之後，操作期間 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) 使用的描述：

1.  針對每個未壓縮的介面，解碼器都會呼叫 [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) 來開始處理，以建立輸出圖片。 當它這麼做時，就會傳送 [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) 結構。
    -   [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo)結構包含目的地緩衝區的索引、一些要傳送下游的資料指標，以及一個指向某個位置的指標，可讓您在其中輸入要讀取之解碼器的一些資料。
    -   附注1：此加速器實際上並不會接收目的地緩衝區索引，因為轉譯器會先轉譯它，然後再繼續下游。
    -   附注2： [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) 在對 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe)的呼叫之間，可以呼叫一次以上。
    -   附注3：在介面作業中不會假設 [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) 和 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) 需要呼叫，才能處理位流中的每個個別圖片。

        [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe)在介面方面的作用，是在索引子與未壓縮表面之間建立關聯性。 它也提供一個方法來撥號裝置磁碟機中的特定函式 (支援在解碼器和設備磁碟機) 之間來回傳遞任意資料的方法。

         (不過，在 DirectX VA 作業中，有如下所述的需求，必須呼叫 [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) 和 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) ，才能處理位流中的每個個別圖片。 ) 

2.  若要將未壓縮的資料傳送至加速器，此解碼會呼叫：
    -   [**IAMVideoAccelerator：： QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) ，以判斷緩衝區是否可安全讀取或寫入。
    -   [**IAMVideoAccelerator：： GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) 可鎖定並取得指定緩衝區的存取權 (如果之前未呼叫此存取權，) 。 **GetBuffer** 也可以用來取得上次未壓縮輸出圖片的複本，該圖片會呼叫 [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) ，並提供尚未針對該目的緩衝區索引呼叫的 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) 。 如果 DDI 傳回所要求緩衝區的 DDERR WASSTILLDRAWING 轉譯狀態，則在 \_ 清除此條件之前，將會在 **GetBuffer** 中運作睡眠迴圈。 為了呼叫 **GetBuffer**，此解碼器將需要 [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) 資料結構中的一些資訊，而這些資訊是透過呼叫 [**IAMVideoAccelerator：： GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo)取得的。
    -   [**IAMVideoAccelerator：： Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) 表示應處理一組壓縮緩衝區中的資料，如 [**AMVABUFFERINFO**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) 資料結構陣列所示。 在此呼叫中，會將函式程式碼 dwFunction 傳遞至驅動程式。 LpPrivateInputData 指標也會傳遞至某些資料以傳送下游，而 lpPrivateOutputData 指標會傳遞至一個位置，讓下游進程可以在其中放置一些資料來讀取該解碼器。
    -   [**IAMVideoAccelerator：： ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) 表示解碼器已完成使用指定的緩衝區，且不再需要鎖定的緩衝區存取。  (如果此解碼器希望繼續使用緩衝區，它可能只會在當時未呼叫 **IAMVideoAccelerator：： ReleaseBuffer** ，因此不需要呼叫 [**IAMVideoAccelerator：： GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) ，直到它真的不會再使用該緩衝區為止。 ) 在呼叫 [**Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) 之後，不應將該緩衝區寫入緩衝區，直到 [**QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) 表示緩衝區可以安全寫入為止。
3.  為了完成目的地緩衝區的輸出處理，此解碼器會呼叫 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe)。 它可以使用此呼叫來傳遞一些任意的資料，基本上這就是此呼叫的結果。 它不會在此呼叫中傳送目的地緩衝區索引，因此它無法精確地向加速器指出完成的目的地緩衝區，除非此指示包含在傳遞的任意資料中。
4.  為了顯示框架，此解碼器會以要顯示的框架索引和包含開始和停止時間戳記的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)結構和相關旗標（例如 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構中的 **DwTypeSpecificFlags** ）和 [**dwInterlaceFlags 結構中的**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) **VIDEOINFOHEADER2** ，來呼叫 [**IAMVideoAccelerator：:D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) 。 在呼叫 **DisplayFrame** 之前，此解碼器必須確認所有會影響框架內容的解壓縮作業都已完成。
5.  最後，在完成所有處理時，此解碼器應該會藉由呼叫 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) 來完成所有剩餘的已開始輸出畫面格，並藉由針對每個未發行緩衝區呼叫 [**IAMVideoAccelerator：： ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) 來釋放其所有鎖定的緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[解碼器介面和規格](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



