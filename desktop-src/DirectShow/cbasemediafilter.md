---
description: CBaseMediaFilter 類別會實 IMediaFilter 介面。
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: 'CBaseMediaFilter 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16225ca289597bd8145e689912fd458a4f29d8aa4cc5ca68d6c3e0d0e3605ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586100"
---
# <a name="cbasemediafilter-class"></a>CBaseMediaFilter 類別

![cbasemediafilter](images/filter05.png)

類別會實 `CBaseMediaFilter` [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) 介面。 針對外掛程式散發者或其他需要支援 **IMediaFilter** 而不支援 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的物件，請使用這個類別。 請勿將這個類別用於篩選。 請改為使用 [**CBaseFilter**](cbasefilter.md) 類別或衍生自 **CBaseFilter** 的基類。



| 受保護的成員變數                                       | 描述                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**m \_ 狀態**](cbasemediafilter-m-state.md)                     | 物件的目前狀態。                                 |
| [**m \_ pClock**](cbasemediafilter-m-pclock.md)                   | 物件參考時鐘的指標。                     |
| [**m \_ tStart**](cbasemediafilter-m-tstart.md)                   | 對應于資料流程時間0的參考時間。            |
| [**m \_ clsid**](cbasemediafilter-m-clsid.md)                     | 物件 (CLSID) 的類別識別碼。                      |
| [**m \_ pLock**](cbasemediafilter-m-plock.md)                     | 重要區段的指標。                               |
| 公用方法                                                   | 描述                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | 函式方法。                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | 函式方法。 虛擬。                                  |
| [**StreamTime**](cbasemediafilter-streamtime.md)                | 抓取目前的資料流程時間。 虛擬。                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | 判斷物件是否為作用中， (執行中或已暫停) 。 |
| IPersist 方法                                                 | 描述                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | 捕獲類別識別碼。                              |
| IMediaFilter 方法                                             | 描述                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | 抓取物件的狀態 (執行中、已停止或已暫停) 。  |
| [**SetSyncSource**](cbasemediafilter-setsyncsource.md)          | 設定物件的參考時鐘。                       |
| [**GetSyncSource**](cbasemediafilter-getsyncsource.md)          | 抓取物件正在使用的參考時鐘。      |
| [**停止**](cbasemediafilter-stop.md)                            | 停止物件。                                            |
| [**暫停**](cbasemediafilter-pause.md)                          | 暫停物件。                                           |
| [**執行**](cbasemediafilter-run.md)                              | 執行物件。                                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




