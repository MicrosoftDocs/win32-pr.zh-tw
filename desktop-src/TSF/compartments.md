---
title: 車廂
description: 車廂
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- 文字服務架構 (TSF) 、區間
- TSF (文字服務架構) 、區間
- 文字服務，區間
- 啟用 TSF 的應用程式，區間
- 車廂
- 文字服務架構 (TSF) 、區間類型
- TSF (文字服務架構) 、區間類型
- 文字服務、區間類型
- 啟用 TSF 的應用程式，區間類型
- 區間類型
- 文字服務架構 (TSF) 、區間變更通知
- TSF (文字服務架構) ，區間變更通知
- 文字服務，區間變更通知
- 啟用 TSF 的應用程式，區間變更通知
- 區間變更通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183260"
---
# <a name="compartments"></a>車廂

## <a name="compartment-types"></a>區間類型

有數種不同類型的區間。 有一個全域區間，而且每個執行緒管理員、檔管理員和內容都可以包含區間。

全域區間可讓用戶端跨進程共用資料。 若要取得全域區間管理員，請呼叫 [**ITfThreadMgr：： GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)。

執行緒管理員包含區間管理員，其中包含每個執行緒的區間。 這可讓您線上程內共用資料。 若要取得執行緒管理員區間管理員，請使用 IID ITfCompartmentMgr 呼叫 **ITfThreadMgr：： QueryInterface** \_ 。

每個建立的檔管理員也都包含區間管理員。 這可讓您在特定檔管理員內共用資料。 若要取得檔管理員區間管理員，請使用 IID ITfCompartmentMgr 呼叫 **ITfDocumentMgr：： QueryInterface** \_ 。

所建立的每個內容也會包含區間管理員。 這可讓您在特定內容中共用資料。 若要取得內容區間管理員，請使用 IID ITfCompartmentMgr 呼叫 **ITfCoNtext：： QueryInterface** \_ 。

## <a name="creating-and-deleting-a-compartment"></a>建立和刪除區間

第一次使用區間 GUID 呼叫 [**ITfCompartmentMgr：： GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) 時，會建立區間。 安裝用戶端應該使用 [**ITfCompartment：： SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)設定區間的初始值。 在設定值之前，區間值是空的。 因此，在呼叫 **GetCompartment** 之前，無法驗證區間是否存在。 為了避免這種情況，安裝用戶端應該將值設定為某個初始值，讓其他用戶端可以判斷區間是否已存在。

[**ITfCompartmentMgr：： ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)方法用來移除區間。 區間的任何現有參考都會標示為無效。

## <a name="obtaining-compartments"></a>取得區間

用戶端可以使用 [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) 介面，藉由呼叫 [**ITfCompartmentMgr：： EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)來列舉區間。 這個方法會提供 **IEnumGUID** 物件，其中包含所有已安裝之區間的 guid。

使用區間 GUID， **ITfCompartmentMgr：： GetCompartment** 可用來取得特定區間。 這個方法會為呼叫端提供可取得及設定區間資料的 [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) 物件。

## <a name="receiving-compartment-change-notifications"></a>接收區間變更通知

當區間的值變更時，TSF manager 會通知任何已安裝的通知接收器，區間已變更。 若要安裝區間變更建議接收器，請建立可執行 [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)的物件。 然後，在要監視的區間物件上，對 IID ITfSource 呼叫 **ITfCompartment：： QueryInterface** ， \_ 以取得 [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) 介面。 現在呼叫 [**ITfSource：： AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) 搭配 IID \_ ITfCompartmentEventSink 和 **ITfCompartmentEventSink** 物件的指標。 當區間的值變更時，會以區間的 GUID 呼叫建議接收器的 [**ITfCompartmentEventSink：： OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) 。 建議接收可呼叫 [**ITfCompartment：： GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) 來取得新值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[**TfClientId**](tfclientid.md)
</dt> <dt>

[**ITfThreadMgr：： GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**ITfCompartment：： SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITfCompartmentEventSink：： OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




