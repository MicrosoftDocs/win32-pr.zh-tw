---
description: 應用程式無法以身歷聲轉譯，除非作業系統指出它會啟用 stereoscopic 3D 顯示行為。 應用程式會根據視窗是否為視窗化或全螢幕，決定是否要以不同的方式呈現 stereoscopic 3D。
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: 以身歷聲轉譯並通知身歷聲狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379c6335e0bd060cf0065fe92bf2ec6c086289c3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108385"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>以身歷聲轉譯並通知身歷聲狀態

應用程式無法以身歷聲轉譯，除非作業系統指出它會啟用 stereoscopic 3D 顯示行為。 應用程式會根據視窗是否為視窗化或全螢幕，決定是否要以不同的方式呈現 stereoscopic 3D。

視窗型應用程式會呼叫 [**IDXGIFactory2：： IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) 方法，以判斷是否要以身歷聲呈現。 全螢幕應用程式會呼叫 [**IDXGIOutput1：： GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) 方法，然後判斷是否有任何傳回的顯示模式支援以身歷聲呈現。 除非您在 *旗標* 參數中指定了 [**DXGI \_ 列舉 \_ 模式 \_ 身歷聲**](dxgi-enum-modes.md)旗標，否則 **GetDisplayModeList1** 方法不會列舉身歷聲模式。 支援身歷聲的視窗式或全螢幕應用程式會先根據 **IDXGIFactory2：： IsWindowedStereoEnabled** 或 **IDXGIOutput1：： GetDisplayModeList1** 方法的呼叫，判斷要以身歷聲轉譯，然後註冊以取得身歷聲狀態變更的通知。 由於應用程式無法依賴通知來指出 stereoscopic 3D 顯示行為的目前狀態，當它收到通知事件或視窗訊息時，必須再次呼叫 **IDXGIFactory2：： IsWindowedStereoEnabled** 或 **IDXGIOutput1：： GetDisplayModeList1** ，以判斷作業系統 stereoscopic 3d 顯示行為的目前狀態。

如果您想要以身歷聲轉譯，則必須註冊身歷聲通知，以知道使用者何時關閉或有身歷聲行為。 您可以註冊應用程式，以透過訊息至視窗或透過事件信號來通知 stereoscopic 3D 狀態變更。 若要註冊以接收關於身歷聲狀態變更之視窗的通知訊息，應用程式會呼叫 [**IDXGIFactory2：： RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) 方法。 若要註冊以透過事件信號接收身歷聲狀態變更的通知，應用程式會呼叫 [**IDXGIFactory2：： RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) 方法。 這兩種方法都會將指標傳回給應用程式用來取消註冊通知的索引鍵值。 若要取消註冊通知，應用程式會將此索引鍵值傳遞給 [**IDXGIFactory2：： UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) 方法。

身歷聲狀態可包含下列元素：

-   使用者設定。

    Windows 使用者可以在主控台的 [變更顯示設定] 中，啟用或停用 [啟用 stereoscopic 3D] 選項的身歷聲顯示。

-   電腦功能和設定，包括圖形介面卡、圖形驅動程式和監視器安裝程式。

[Direct3D 11.1 Simple 身歷聲3D 範例示範](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample)如何新增 stereoscopic 3d 效果，以及如何回應系統身歷聲變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI 1.2 改進](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
