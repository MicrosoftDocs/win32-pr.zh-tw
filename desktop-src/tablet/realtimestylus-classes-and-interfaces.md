---
description: 本章節包含有關即時手寫筆中所使用之介面和類別的資訊。
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: RealTimeStylus 類別和介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd842219a23accc076ff7fdc8564ccb3ce0c472cb7e26ab036f1048456461f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589948"
---
# <a name="realtimestylus-classes-and-interfaces"></a>RealTimeStylus 類別和介面

本章節包含有關即時手寫筆中所使用之介面和類別的資訊。

> [!Note]  
> 即時手寫筆類別和介面不符合自動化規範。

 

## <a name="in-this-section"></a>本節內容



| 類別                                                      | 描述                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**RealTimeStylus 類別**](realtimestylus-class.md)       | 實行 [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) 介面。<br/>                 |
| [**DynamicRenderer 類別**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | 實行 [**IDynamicRenderer 介面**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) 介面。<br/>     |
| [**GestureRecognizer 類別**](gesturerecognizer-class.md) | 實行 [**IGestureRecognizer 介面**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) 介面。<br/> |
| [**StrokeBuilder 類別**](strokebuilder-class.md)         | 實行 [**IStrokeBuilder 介面**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) 介面。<br/>         |



 

## <a name="interfaces"></a>介面



| 介面                                                                          | 描述                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDynamicRenderer 介面**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | 公開方法，可讓您在資料由 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件處理時，即時控制手寫筆資料的顯示。<br/> |
| [**IGestureRecognizer 介面**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | 公開方法，讓您能夠辨識手寫筆手勢，並讓您將資料新增至輸入佇列，以回應事件。<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | 即時處理來自數位板的手寫筆封包資料。<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | 擴充 IRealTimeStylus 介面。<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | 擴充 IRealTimeStylus 介面。<br/>                                                                                                                                           |
| [**IRealTimeStylusSynchronization 介面**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | 同步處理對 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件的存取。<br/>                                                                                          |
| [**IStrokeBuilder 介面**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | 公開可讓您以程式設計方式建立筆劃的方法。<br/>                                                                                                              |
| [**IStylusPlugin 介面**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | 公開方法，讓您可以接收事件的通知，並根據這些事件執行自訂處理。<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | 表示可以加入至 [**RealTimeStylus 類別**](realtimestylus-class.md) 非同步外掛程式集合的非同步外掛程式。<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | 表示可以加入至 [**RealTimeStylus 類別**](realtimestylus-class.md) 同步外掛程式集合的同步外掛程式。<br/>                                   |



 

## <a name="return-values"></a>傳回值

COM 程式庫中的方法會傳回 **HRESULT** 的值。 除非另有說明，否則 **HRESULT** 值的意義如下表所述。



| HRESULT 值                                   | 描述                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ 確定<br/>                                | 成功。<br/>                                                                      |
| E \_ 指標<br/>                           | 輸入或輸出參數的至少一個指標 () 無效。<br/> |
| E \_ INVALIDARG<br/>                        | 成員嘗試傳入不正確引數。<br/>                              |
| E \_ 筆墨 \_ 例外狀況<br/>                    | 發生例外狀況。<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | 系統無法配置記憶體來完成操作。<br/>                      |
| E \_ 失敗<br/>                              | 發生未指定的失敗。<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | 成員嘗試使用不正確作業。<br/>                                 |
| TPC \_ E \_ 無效 \_ 模式<br/>                | 成員嘗試使用不正確模式。<br/>                                      |
| TPC \_ E \_ 不正確設定 \_<br/>       | 成員嘗試使用不正確設定。<br/>                             |
| TPC \_ E \_ 不正確封 \_ 包 \_ 描述<br/> | 成員嘗試使用不正確封包描述。<br/>                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[RealTimeStylus 參考](realtimestylus-reference.md)
</dt> </dl>

 

 
