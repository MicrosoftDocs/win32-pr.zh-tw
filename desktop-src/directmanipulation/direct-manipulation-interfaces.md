---
description: 本節所包含的主題會提供直接操作介面的參考規格。
ms.assetid: 03680CE5-A858-4876-B41C-6F2E08C02C22
title: 直接操作介面
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5eb3ae1b06cd940adc126d53a9cce58e4b6b5935
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467662"
---
# <a name="direct-manipulation-interfaces"></a>直接操作介面

本節所包含的主題會提供 [直接操作](direct-manipulation-portal.md) 介面的參考規格。

> [!Note]  
> 在執行 [直接操作](direct-manipulation-portal.md) 物件時，請確定 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 實作為透過安全線程的參考計數來支援多執行緒處理。 如需詳細資訊，請參閱 [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) 和 [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement)。

## <a name="in-this-section"></a>本節內容

| 主題                                                                                                       | 描述                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectManipulationAutoScrollBehavior**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationautoscrollbehavior)<br/>           | 表示在使用指定軸或軸的界限時，內容的自動滾動動畫行為。<br/>                                                                                                                                                   |
| [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)<br/>                           | 表示組合物件，此物件會將操作內容與繪圖介面（例如 [**canvas**](/uwp/api/Windows.UI.Xaml.Controls.Canvas)）產生關聯。<br/> |
| [**IDirectManipulationCompositor2**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor2)<br/>                         | 表示組合器物件，此物件會將操作內容與跨多個進程的繪圖介面產生關聯。<br/>                                                                                                                                               |
| [**IDirectManipulationContent**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcontent)<br/>                                 | 將內容封裝在一個區內，其中內容代表在物件區內裁剪的視覺化介面。<br/>                                                                                                                                                    |
| [**IDirectManipulationDeferContactService**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationdefercontactservice)<br/>         | 表示用來管理連絡人與視口之間關聯的服務。<br/>                                                                                                                                                                                  |
| [**IDirectManipulationDragDropBehavior**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationdragdropbehavior)<br/>               | 表示拖放互動的行為，這些行為是透過跨幻燈片或按住手勢來觸發。 <br/>                                                                                                                                              |
| [**IDirectManipulationDragDropEventHandler**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationdragdropeventhandler)<br/>       | 定義處理拖放行為事件的方法。<br/>                                                                                                                                                                                                              |
| [**IDirectManipulationFrameInfoProvider**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider)<br/>             | 代表時間的物件，這個物件會測量應用程式所使用之組合基礎結構的延遲，並提供此資料以進行 [直接操作](direct-manipulation-portal.md)。 <br/>                                                            |
| [**IDirectManipulationInteractionEventHandler**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationinteractioneventhandler)<br/> | 定義在偵測到互動時處理互動的方法。<br/>                                                                                                                                                                                                    |
| [**IDirectManipulationManager**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationmanager)<br/>                                 | 提供可供用戶端應用程式使用的所有 [直接操作](direct-manipulation-portal.md) 功能和 api 的存取權。<br/>                                                                                                                           |
| [**IDirectManipulationManager2**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationmanager2)<br/>                               | 擴充 [**IDirectManipulationManager**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationmanager) 介面，以提供用戶端應用程式可用之所有 [直接操作](direct-manipulation-portal.md) 功能和 api 的存取權。 <br/>                              |
| [**IDirectManipulationManager3**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationmanager3)<br/>                               | 擴充 [**IDirectManipulationManager2**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationmanager2) 介面，以提供用戶端應用程式可用之所有 [直接操作](direct-manipulation-portal.md) 功能和 api 的存取權。 <br/>                            |
| [**IDirectManipulationPrimaryContent**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationprimarycontent)<br/>                   | 封裝區內的主要內容。<br/>                                                                                                                                                                                                               |
| [**IDirectManipulationUpdateHandler**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationupdatehandler)<br/>                     | 定義處理操作更新事件的方法。<br/>                                                                                                                                                                                                          |
| [**IDirectManipulationUpdateManager**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationupdatemanager)<br/>                     | 管理組合器更新如何傳送至 [直接操作](direct-manipulation-portal.md)。<br/>                                                                                                                                                                 |
| [**IDirectManipulationViewport**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationviewport)<br/>                               | 定義視窗內的區域 (稱為可接收和處理使用者互動輸入的區) 。 <br/>                                                                                                                                   |
| [**IDirectManipulationViewport2**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationviewport2)<br/>                             | 提供在視口上的行為管理。 行為會影響 [直接操作](direct-manipulation-portal.md) 工作流程特定部分的功能。 <br/>                                                                                 |
| [**IDirectManipulationViewportEventHandler**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationviewporteventhandler)<br/>       | 定義處理視口狀態和更新事件的方法。<br/>                                                                                                                                                                                           |
