---
description: CMediaEvent 類別提供雙重介面 IMediaEvent 之 IDispatch 方法的基類實作為基底類別。 它會將 IMediaEvent 介面的屬性和方法保留為純虛擬。
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: CMediaEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195768"
---
# <a name="cmediaevent-class"></a>CMediaEvent 類別

![cmediaevent 類別階層](images/cutil03.png)

`CMediaEvent`類別提供雙重介面 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)之 **IDispatch** 方法的基類實作為基底類別。 它會將 **IMediaEvent** 介面的屬性和方法保留為純虛擬。

`CMediaEvent`類別也提供衍生自 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)之 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)介面的基類實作為基底類別。

[**CMediaEvent：： GetIDsOfNames**](cmediaevent-getidsofnames.md)、 [**CMediaEvent：： GetTypeInfo**](cmediaevent-gettypeinfo.md)、 [**CMediaEvent：： GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)和 [**CMediaEvent：： Invoke**](cmediaevent-invoke.md)成員函式是 **IDispatch** 介面的標準，使用 [**CBaseDispatch**](cbasedispatch.md)類別 (和類型程式庫) 來剖析命令，並將其傳遞給 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)介面的純虛擬方法。



| 成員函數                                         | Description                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | 結構 **CMediaEvent** 物件。                                                                                                                                                          |
| IDispatch 方法                                        | Description                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | 將單一成員和一組選擇性的參數對應至一組對應的整數分派識別碼，可在後續呼叫 **IDispatch：： Invoke** 方法時使用。 |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | 抓取類型資訊物件，此物件會捕獲介面的類型資訊。                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | 抓取物件所提供的類型資訊介面數目。                                                                                                                    |
| [**調用**](cmediaevent-invoke.md)                     | 提供物件所公開的屬性和方法的存取權。                                                                                                                               |



 

 

 



