---
description: 本主題說明如何撰寫 DirectShow 的自訂影片轉譯器。
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: 替代影片轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd105f406e1b39d998a027a915621f214ec2e769f373912a1e9e8525573f31aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074802"
---
# <a name="alternative-video-renderers"></a>替代影片轉譯器

本主題說明如何撰寫 DirectShow 的自訂影片轉譯器。

> [!Note]  
> 建議您撰寫適用于影片混合轉譯器的外掛程式配置器， (VMR) 或 [**增強的影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR) ，而不是撰寫自訂影片轉譯器。 這種方法可提供 VMR/EVR 的所有優點，包括支援 DirectX Video 加速 (DXVA) 、硬體去交錯和框架逐步執行，而且可能比自訂影片轉譯器更健全。 如需詳細資訊，請參閱下列主題：
>
> -   [VMR Renderless 播放模式 (自訂配置器-展示者) ](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [如何撰寫 EVR 展示者](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>撰寫替代轉譯器

Microsoft DirectShow 提供以視窗為基礎的影片轉譯器;它也會在執行時間安裝中提供全螢幕轉譯器。 您可以使用 DirectShow 基類來撰寫替代的影片轉譯器。 若要讓替代轉譯器與 DirectShow 型應用程式正確互動，轉譯器必須遵守本文中所述的指導方針。 您可以使用 [**CBaseRenderer**](cbaserenderer.md) 和 [**CBaseVideoRenderer**](cbasevideorenderer.md) 類別，在執行替代的影片轉譯時，協助您遵循這些指導方針。 由於持續開發 DirectShow，請定期審核您的實施，以確保轉譯器與最新版本的 DirectShow 相容。

本主題討論轉譯器負責處理的許多通知。 DirectShow 通知的簡短評論可能有助於設定階段。 在 DirectShow 中，基本上有三種通知：

-   *資料流程通知* 是在媒體資料流程中發生的事件，會從一個篩選準則傳遞到下一個篩選器。 這些可以是開始排清、結束排清或結束資料流程通知，並藉由在下游篩選的輸入 pin 上呼叫適當的方法來傳送 (例如 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)) 。
-   *篩選圖形通知*，這是從篩選傳送至篩選 Graph 管理員（例如 [**EC \_ 完成**](ec-complete.md)）的事件。 這可透過在篩選 Graph 管理員上呼叫 [**IMediaEventSink：： Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)方法來完成。
-   *代理程式更新*，由控制應用程式從篩選 Graph 管理員抓取。 應用程式會在篩選 Graph 管理員上呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)方法，以取得這些事件。 通常，篩選 Graph 管理員會將它所收到的事件傳遞至應用程式。

本主題討論轉譯器篩選器在處理它所接收的串流通知，以及傳送適當的篩選圖形通知時的責任。

## <a name="handling-end-of-stream-and-flushing-notifications"></a>處理資料流程結束和清除通知

資料流程結束通知會從上游篩選開始 (例如來源篩選準則，) 篩選器偵測到它無法傳送任何資料。 它會通過圖形中的每個篩選器，最後結束于轉譯器，而該轉譯器負責後續將 [**EC \_ 完成**](ec-complete.md)通知傳送至篩選 Graph 管理員。 轉譯器在處理這些通知時有特殊責任。

當上游篩選器呼叫它的輸入釘選 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法時，轉譯器會接收資料流程結束通知。 轉譯器應該記下此通知，然後繼續轉譯它已收到的任何資料。 一旦收到所有剩餘的資料，轉譯器就會將 [**EC \_ 完成**](ec-complete.md)通知傳送至篩選 Graph 管理員。 每次在每次到達資料流程結尾時，轉譯器都應該只傳送一次 **EC \_ 完成** 通知。 此外，只有在執行篩選圖形時，才必須傳送 **EC \_ 完全** 通知。 因此，當來源篩選傳送資料流程結束時，如果篩選圖形暫停，則在最後執行篩選圖形之前，不應傳送 **EC \_ 完成** 。

[**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)或 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)方法在結束資料流程通知之後的任何呼叫都應遭到拒絕。 **E \_** 在此情況下，未預期的是最適當的錯誤訊息。

當篩選圖形停止時，應該清除任何快取的資料流程結束通知，而不會在下次啟動時重新傳送。 這是因為篩選 Graph 管理員一律會在執行之前暫停所有篩選，以便進行適當的排清。 因此，例如，如果已暫停篩選圖形並收到資料流程結束通知，然後篩選圖形已停止，則轉譯器在後續執行時，不應傳送 [**EC \_ 完成**](ec-complete.md) 通知。 如果未進行任何搜尋，來源篩選器會在執行狀態之前的暫停狀態期間，自動傳送另一個結束資料流程的通知。 另一方面，如果在篩選圖形停止時發生搜尋，則來源篩選可能會有要傳送的資料，因此不會傳送資料流程結束通知。

影片轉譯器通常相依于資料流程的結束通知，而不是傳送 [**EC \_ 完成**](ec-complete.md) 通知。 例如，如果資料流程已完成播放 (也就是已) 傳送資料流程結束通知，然後將另一個視窗拖曳到 [影片轉譯器] 視窗上，則會產生許多的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 視窗訊息。 執行影片轉譯器的一般作法是避免在收到 **WM \_ 油漆** 訊息時重新繪製目前的框架 (根據假設將會) 收到另一個要繪製的框架。 但是，當傳送資料流程結束通知時，轉譯器會處於等候狀態;它仍在執行中，但卻知道它將不會收到任何額外的資料。 在這些情況下，轉譯器通常會將播放區域呈現為黑色。

處理清除是轉譯器的額外複雜。 清除會透過一對稱為 [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)和 [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)方法來執行。 排清程式基本上是轉譯器必須處理的其他狀態。 來源篩選器在不呼叫 **EndFlush** 的情況下呼叫 **BeginFlush** 是不合法的，所以希望狀態是簡短且離散的;不過，轉譯器必須正確處理在排清轉換期間收到的資料或通知。

呼叫 [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 之後所收到的任何資料，都應該藉由傳回 **\_ FALSE** 來立即予以拒絕。 此外，在清除轉譯器時，也應該清除任何快取的資料流程結束通知。 轉譯器通常會在回應搜尋時進行清除。 排清可確保在傳送新的範例之前，會從篩選圖形清除舊的資料。  (通常會在資料流程的兩個區段之前逐一播放，最好是透過延後的命令來處理，而不是等候一個區段完成，然後再發出 seek 命令。 ) 

## <a name="handling-state-changes-and-pause-completion"></a>處理狀態變更並暫停完成

轉譯器篩選器的狀態變更時，與篩選圖形中的任何其他篩選器的行為相同，但有下列例外狀況。 在暫停之後，轉譯器會將一些資料排入佇列，準備好在後續執行時進行轉譯。 當影片轉譯器停止時，它會保留在此已排入佇列的資料。 這是 DirectShow 規則的例外狀況，篩選圖形停止時，篩選器不應保留任何資源。

這個例外狀況的原因是，藉由保留資源，轉譯器一律會有一個影像，以便在收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時重新繪製視窗。 它也有一個可滿足方法（例如 [**CBaseControlVideo：： GetStaticImage**](cbasecontrolvideo-getstaticimage.md)）的影像，可要求目前映射的複本。 保存資源的另一項影響是將配置器停止已取消認可，進而讓下一次狀態變更的執行速度變得更快，因為映射緩衝區已配置。

只有在執行時，影片轉譯器才會轉譯和發行範例。 在暫停時，篩選可能會轉譯 (例如，在視窗) 中繪製靜態海報影像時，不應該釋出它們。 音訊轉譯器不會在暫停 (的情況下進行轉譯，不過它們可以執行其他活動，例如) 的準備 wave 裝置。 您可以藉由將範例中的資料流程時間與傳遞給 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 方法的參考時間結合，來取得應轉譯樣本的時間。 轉譯器應該拒絕開始時間小於或等於結束時間的樣本。

當應用程式暫停篩選圖形時，不會從 [**IMediaControl：:P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) 方法傳回篩選圖形，直到轉譯器有資料佇列為止。 為了確保這一點，當轉譯器暫停時，如果沒有等待轉譯的資料，它應該會傳回 \_ FALSE。 如果資料已排入佇列，則可能會 **傳回 \_ [確定]**。

篩選 Graph 管理員會在暫停篩選圖形時，檢查所有傳回值，以確保轉譯器已將資料排入佇列。 如果有一或多個篩選準則未就緒，則篩選 Graph 管理員會藉由呼叫 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)來輪詢圖形中的篩選。 **>Getstate** 方法會使用超時參數。 篩選準則 (通常是在 **>getstate** 方法過期時，仍在等候資料抵達的轉譯器) 會傳回 **VFW \_ S \_ 狀態 \_ 中繼**。 當資料抵達轉譯器之後， **>getstate** 應該會立即傳回，而且可以是 **\_ OK**。

在 [中繼] 和 [已完成] 狀態中，報告的篩選狀態將會 \_ 暫停狀態。 只有傳回值會指出篩選準則是否真的就緒。 如果轉譯器正在等候資料到達，則其來源篩選準則會傳送資料流程結束通知，然後也應完成狀態變更。

一旦所有篩選準則都有等候轉譯的資料，篩選圖形將會完成其暫停狀態變更。

## <a name="handling-termination"></a>處理終止

影片轉譯器必須正確地處理來自使用者的終止事件。 這表示會正確地隱藏視窗，並知道後續會強制顯示視窗時該怎麼辦。 此外，當轉譯器從篩選圖形中移除時，當轉譯器從篩選圖形中移除時，影片轉譯器必須將篩選 Graph (管理員通知) 以釋放資源。

如果使用者按下 ALT + F4) 來關閉影片視窗 (例如，慣例是立即隱藏視窗，然後將 [**EC \_ USERABORT**](ec-userabort.md)通知傳送至篩選 Graph 管理員。 此通知會傳遞至應用程式，這將會停止圖表播放。 傳送 **EC \_ USERABORT** 之後，影片轉譯器應該拒絕任何其他傳遞給它的範例。

圖形停止的旗標應該留在轉譯器之前，直到它之後停止為止，此時應該重設，讓應用程式可以覆寫使用者動作，並視需要繼續播放圖形。 如果影片正在執行時按下 ALT + F4，則會隱藏視窗，並會拒絕所有更進一步的範例。 如果後續顯示視窗 (可能是透過 [**IVideoWindow：:p 顯示) \_ 可見**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) ，則不應產生任何 [**EC 重新 \_ 繪製**](ec-repaint.md) 通知。

影片轉譯器也應該在影片轉譯器結束時，將 [ [**EC \_ 視窗] \_**](ec-window-destroyed.md) 終結通知傳送至篩選圖形。 事實上，最好是在使用 null 參數呼叫轉譯器的 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法時進行處理， (表示轉譯器即將從篩選圖形) 中移除，而不是等到實際的影片視窗終結為止。 傳送此通知可讓篩選 Graph 管理員中的外掛程式散發者，將相依于視窗焦點的資源傳遞給其他篩選器，例如音訊裝置。

## <a name="handling-dynamic-format-changes"></a>處理動態格式變更

在某些情況下，轉譯器的上游篩選可能會在播放影片時嘗試變更影片格式。 它最常是起始動態格式變更的影片解壓縮程式。

嘗試動態變更格式的上游篩選器應該一律呼叫轉譯器輸入釘選上的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法。 影片轉譯器對於其應該支援的動態格式變更類型有一些一點時間。 它至少應該允許上游篩選器變更調色板。 當上游篩選變更媒體類型時，它會將媒體類型附加至以新格式傳遞的第一個範例。 如果轉譯器在佇列中保存範例以供轉譯，則在轉譯具有類型變更的範例之前，不應該變更格式。

影片轉譯器也可以從解碼器要求格式變更。 例如，它可能會要求解碼器提供具有負面 **biHeight** 的 DirectDraw 相容格式。 當轉譯器暫停時，它應該呼叫上游釘選上的 [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ，以查看該解碼器可以提供的格式。 但是，此解碼器可能不會列舉其可接受的所有型別，因此，轉譯器應該提供某些型別，即使該解碼器沒有通告它們也一樣。

如果解碼器可以切換為要求的格式，則會從 [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)傳回 **S \_ OK** 。 然後，轉譯器會將新的媒體類型附加至上游配置器上的下一個媒體範例。 若要這樣做，轉譯器必須提供自訂配置器，它會執行私用方法，以將媒體類型附加至下一個範例。  (在此私用方法中，請呼叫 [**IMediaSample：： SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) 來設定類型。 ) 

轉譯器的輸入圖釘應該會在 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法中傳回轉譯器的自訂配置器。 覆寫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) ，使上游篩選器不使用轉譯器的配置器時，它就會失敗。

使用某些解碼器時，若將 **biHeight** 設定為正數，則會讓解碼器將影像向下繪製。  (此項不正確，則應視為解碼器中的 bug。 ) 

每當影片轉譯器偵測到格式變更時，它應該會傳送 [**EC \_ 顯示 \_ 變更**](ec-display-changed.md) 的通知。 大部分的影片轉譯器會在連接期間挑選格式，以便透過 GDI 有效率地繪製格式。 如果使用者在不重新開機電腦的情況下變更目前的顯示模式，轉譯器可能會發現本身的影像格式不正確，而且應該傳送此通知。 第一個參數應該是需要重新連接的 pin。 篩選 Graph 管理員將會排列要停止的篩選圖形，以及重新連接的 pin。 在後續的重新連接期間，轉譯器可以接受更適當的格式。

每當影片轉譯器偵測到資料流程中的調色板變更時，就應該將 [EC 選擇區變更] 通知傳送至篩選 Graph 管理員。 [**\_ \_**](ec-palette-changed.md) DirectShow 影片轉譯器會偵測調色板是否已真正變更為動態格式。 影片轉譯器不只會篩選出已傳送的 EC 小 **\_ 元件 \_ 變更** 通知數目，還能減少所需的調色板建立、安裝和刪除的數量。

最後，影片轉譯器也可以偵測到影片的大小已變更，在這種情況下，它應該會傳送 [**EC \_ 影片 \_ 大小 \_ 變更**](ec-video-size-changed.md) 的通知。 應用程式可能會使用此通知來協商複合檔案中的空間。 實際的影片尺寸可透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 控制項介面取得。 DirectShow 轉譯器會在傳送這些事件之前，偵測影片的大小是否真的變更。

## <a name="handling-persistent-properties"></a>處理持續性屬性

透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 和 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面設定的所有屬性都是在連接之間保持一致。 因此，中斷和重新連接轉譯器應該不會對視窗大小、位置或樣式顯示任何影響。 但是，如果影片尺寸在連接之間變更，轉譯器應該將來源和目的地矩形重設為其預設值。 來源和目的地位置是透過 **IBasicVideo** 介面進行設定。

[**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)和 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)都提供足夠的屬性存取權，以允許應用程式以持續格式儲存和還原介面中的所有資料。 當應用程式必須在編輯會話期間儲存篩選圖形的確切設定和屬性，並于稍後還原這些應用程式時，這將會很有用。

## <a name="handling-ec_repaint-notifications"></a>處理 EC 重新 \_ 繪製通知

只有當轉譯器暫停或停止時，才會傳送 [**EC 重新 \_ 繪製**](ec-repaint.md) 通知。 此通知會向篩選器發出轉譯器要求資料的 Graph 管理員。 如果篩選圖形在收到其中一個通知時停止，則會暫停篩選圖形、等候所有篩選器接收資料 (呼叫 [**>getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)) ，然後再將它停止。 停止時，影片轉譯器應該會保留影像，以便可以處理後續的 [**WM \_ 繪製**](/windows/desktop/gdi/wm-paint) 訊息。

因此，如果影片轉譯器在停止或暫停時收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)訊息，而且沒有任何用來繪製其視窗的內容，則它應該會將 [**EC 重新 \_ 繪製**](ec-repaint.md)傳送給篩選 Graph 管理員。 如果在暫停時收到 **EC 重新 \_ 繪製** 通知，則篩選 Graph 管理員會使用目前的位置來呼叫 [**IMediaPosition：:p \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) ]， (也就是搜尋目前的位置) 。 這會導致來源篩選器排清篩選圖形，並讓新的資料透過篩選圖形傳送。

轉譯器一次只能傳送這些通知的其中一個。 因此，一旦轉譯器傳送通知，就應該確保在傳遞一些範例之前，不再傳送任何資訊。 傳統的作法是使用旗標來表示可以傳送重繪，這會在系統傳送 [**EC 重新 \_ 繪製**](ec-repaint.md) 通知之後關閉。 此旗標應該在資料傳遞之後，或在輸入釘選時重設，但如果輸入 pin 上有信號結束資料流程，則應該重設。

如果轉譯器不會監視其 [**EC 重新 \_ 繪製**](ec-repaint.md)通知，則會使用 **EC 重新 \_ 繪製** 要求將篩選準則 Graph 管理員 (這對處理) 而言相當昂貴。 例如，如果轉譯器沒有要繪製的影像，而另一個視窗是在整個拖曳作業中拖曳到轉譯器的整個視窗，轉譯器會接收多個 [**WM \_ 繪製**](/windows/desktop/gdi/wm-paint) 訊息。 只有第一個會從轉譯器產生 **EC 重新 \_ 繪製** 事件通知 Graph 管理員。

轉譯器應該將其輸入的 pin 當作第一個參數傳送給 [**EC 重新 \_ 繪製**](ec-repaint.md) 通知。 如此一來，就會查詢附加的輸出圖釘以進行 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)，並在支援時，先將 **EC 重新 \_ 繪製** 通知傳送至該處。 這可讓輸出圖釘在必須接觸篩選圖形之前處理重繪。 如果篩選圖形已停止，則不會執行此操作，因為已取消認可轉譯器配置器不會提供任何緩衝區。

如果輸出 pin 無法處理要求，且篩選圖形正在執行，則會忽略 [**EC 重新 \_ 繪製**](ec-repaint.md) 通知。 輸出 pin 必須從 [**IMediaEventSink：： Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)傳回 **S \_ OK** ，表示它已成功處理重新繪製要求。 輸出的 pin 將會在篩選 Graph 管理員工作者執行緒上呼叫，以避免轉譯器直接呼叫輸出釘選，因此 >iaas 可避開任何鎖死問題。 如果篩選圖形已停止或暫停，而且輸出不會處理要求，則會完成預設處理。

## <a name="handling-notifications-in-full-screen-mode"></a>在 Full-Screen 模式中處理通知

[**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)外掛程式散發者 (PID) 在篩選圖形中管理全螢幕播放。 它會針對專家的全螢幕轉譯器交換影片轉譯器、將轉譯器的視窗延展至全螢幕，或讓轉譯器直接執行全螢幕播放。 若要在全螢幕通訊協定中互動，影片轉譯器應在每次啟用或停用它的視窗時傳送 [**EC \_ 啟動**](ec-activate.md) 通知。 換句話說，系統應該會針對轉譯器收到的每個 WM ACTI加值稅EAPP 訊息傳送 **EC \_ 啟動** 通知 \_ 。

在全螢幕模式中使用轉譯器時，這些通知會管理切換進入和離開該全螢幕模式。 視窗停用通常發生于使用者按下 ALT + TAB 切換至另一個視窗時，DirectShow 的全螢幕轉譯器會用來做為提示，以回到一般轉譯模式。

當您在切換離開全螢幕模式時，將 [**ec \_ 啟動**](ec-activate.md)通知傳送至篩選 Graph 管理員時，篩選 Graph 管理員會將 [**ec \_ 全螢幕 \_ 遺失**](ec-fullscreen-lost.md)通知傳送至控制應用程式。 例如，應用程式可能會使用此通知來還原全螢幕按鈕的狀態。 **EC \_ 啟動** 通知是由 DirectShow 在內部使用，以管理從影片轉譯器提示的全螢幕切換。

## <a name="summary-of-notifications"></a>通知摘要

此區段會列出轉譯器可以傳送的篩選圖形通知。



| 事件通知                                        | 描述                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ 啟用**](ec-activate.md)                       | 由影片轉譯器針對每個所接收的 WM ACTI加值稅EAPP 訊息，以全螢幕轉譯模式傳送 \_ 。                                                                                                  |
| [**EC \_ 完成**](ec-complete.md)                       | 在轉譯所有資料之後，由轉譯器傳送。                                                                                                                                               |
| [**EC \_ 顯示 \_ 已變更**](ec-display-changed.md)        | 顯示格式變更時由影片轉譯器傳送。                                                                                                                                            |
| [**\_ \_ 已變更 EC 元件**](ec-palette-changed.md)        | 每當影片轉譯器偵測到資料流程中的調色板變更時傳送。                                                                                                                            |
| [**EC 重新 \_ 繪製**](ec-repaint.md)                         | 當 \_ 收到 WM 油漆訊息且沒有可顯示的資料時，由已停止或暫停的影片轉譯器傳送。 這會導致篩選 Graph 管理員產生要繪製至顯示器的框架。 |
| [**EC \_ USERABORT**](ec-userabort.md)                     | 由影片轉譯器傳送以表示使用者要求的關閉 (例如，關閉影片視窗) 的使用者。                                                                               |
| [**EC \_ 影片 \_ 大小 \_ 已變更**](ec-video-size-changed.md) | 每當偵測到原生影片大小變更時，由影片轉譯器傳送。                                                                                                                       |
| [**EC \_ 視窗已 \_ 損毀**](ec-window-destroyed.md)      | 在移除或終結篩選時由影片轉譯器傳送，讓相依于視窗焦點的資源可以傳遞給其他篩選器。                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫影片轉譯器](writing-video-renderers.md)
</dt> </dl>

 

 
