---
description: IAMTimelineObj 介面提供在 DirectShow 編輯服務 (DES) 中操作時間軸物件的方法。
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: 'IAMTimelineObj 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4a987cfd0f08311a0e7a233ab479e5cdbe2fc649fd521ad4f4ed1b37b6df6d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428158"
---
# <a name="iamtimelineobj-interface"></a>IAMTimelineObj 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineObj`介面提供在[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中操作時間軸物件的方法。 所有時程表物件都會執行此方法，包括來源、效果、轉換、追蹤、群組和組合物件。 藉由呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法來建立時間軸物件。

## <a name="members"></a>成員

**IAMTimelineObj** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineObj** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineObj** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | 不支援。<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | 將指定的開始和停止時間四捨五入至最接近的框架界限。<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | 將指定的開始和停止時間（指定為 [**REFTIME**](reftime.md) 值）四捨五入到最接近的框架界限。<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | 不支援。<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | 不支援。<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | 不支援。<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | 抓取物件所產生的識別碼。<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | 不支援。<br/>                                                                                                              |
| [**GetLocked**](iamtimelineobj-getlocked.md)                   | 抓取物件的編輯狀態 (鎖定或解除鎖定) 。<br/>                                                                  |
| [**GetMuted**](iamtimelineobj-getmuted.md)                     | 抓取物件的已靜音狀態。<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | 抓取物件的屬性 setter。<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | 抓取物件的開始和停止時間，相對於物件的父系。<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | 以 [**REFTIME**](reftime.md) 值形式抓取物件的開始和停止時間。<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | 捕獲與這個物件相關聯的子物件。<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | 抓取與這個時間軸物件相關聯的子物件的 GUID。<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | 以 **BSTR** 值形式抓取子物件的 GUID。<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | 判斷是否已設定物件的子物件指標。<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | 不支援。<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | 抓取物件的型別。<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | 抓取應用程式定義的持續性資料。<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | 抓取物件的應用程式定義識別碼。<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | 抓取物件的應用程式定義名稱。<br/>                                                                            |
| [**移除**](iamtimelineobj-remove.md)                         | 從時間軸移除此物件，以便在其他地方 reinsertion。<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | 從時間軸中永久移除這個物件，包括子物件和子系。<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | 未實作。<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | 未實作。<br/>                                                                                                            |
| [**SetLocked**](iamtimelineobj-setlocked.md)                   | 將物件的編輯狀態設定為 [已鎖定] 或 [已解除鎖定]。<br/>                                                                      |
| [**SetMuted**](iamtimelineobj-setmuted.md)                     | 設定物件的已靜音狀態。<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | 設定物件的屬性 setter。<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | 設定物件的開始和停止時間（相對於時程表）。<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | 將物件的開始和停止時間設定為 **REFTIME** 值。<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | 不支援。<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | 指定與這個物件相關聯之子物件的全域唯一識別碼 (GUID) 。<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | 將子物件的 GUID 指定為 **BSTR** 值。<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | 不支援。<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | 設定應用程式定義的持續性資料。<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | 設定物件的應用程式定義識別碼。<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | 設定物件的應用程式定義名稱。<br/>                                                                            |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
