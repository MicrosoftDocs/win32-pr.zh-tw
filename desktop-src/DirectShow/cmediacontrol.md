---
description: CMediaControl 類別提供雙重介面 IMediaControl 之 IDispatch 方法的基類處理。 它會將 IMediaControl 介面的屬性和方法保留為純虛擬。
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: CMediaControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853479"
---
# <a name="cmediacontrol-class"></a>CMediaControl 類別

![cmediacontrol 類別階層](images/cutil02.png)

`CMediaControl`類別提供雙重介面 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)之 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)方法的基類處理。 它會將 **IMediaControl** 介面的屬性和方法保留為純虛擬。

篩選圖形管理員通常是唯一會執行 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 介面的物件。  (篩選準則會執行由 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)繼承的 [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)介面，以從篩選圖形管理員接收控制命令 ) 。因此，此類別庫的限制僅供篩選開發人員使用。

[**CMediaControl：： GetIDsOfNames**](cmediacontrol-getidsofnames.md)、 [**CMediaControl：： GetTypeInfo**](cmediacontrol-gettypeinfo.md)、 [**CMediaControl：： GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)和 [**CMediaControl：： Invoke**](cmediacontrol-invoke.md)成員函式是使用 [**CBaseDispatch**](cbasedispatch.md)類別 (的 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)方法的標準實，而類型程式庫) 來剖析命令並傳遞給 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)介面的純虛擬方法。

Odl 中定義的 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 方法會保留為純虛擬。



| 成員函數                                           | Description                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | 結構 **CMediaControl** 物件。                                                                                                                                                                                                  |
| IDispatch 方法                                          | Description                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | 將單一成員和一組選擇性的參數對應至一組對應的整數分派識別碼 (Dispid) ，可在後續呼叫 [**CMediaControl：： Invoke**](cmediacontrol-invoke.md) 方法期間使用。 |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | 抓取類型資訊物件，此物件可以取得介面的類型資訊。                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | 抓取物件所提供的類型資訊介面數目。                                                                                                                                                              |
| [**調用**](cmediacontrol-invoke.md)                     | 提供物件所公開的屬性和方法的存取權。                                                                                                                                                                         |



 

 

 
