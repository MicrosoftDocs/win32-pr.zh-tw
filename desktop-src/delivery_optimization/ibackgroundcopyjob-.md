---
title: 'IBackgroundCopyJob 介面 (>deliveryoptimization .h) '
description: 使用 IBackgroundCopyJob 介面將檔案新增至作業、設定作業的優先權層級、判斷作業的狀態，以及啟動和停止作業。
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04572f11afd51c3354c5adabd9950e2a3942287a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025006"
---
# <a name="ibackgroundcopyjob-interface"></a>IBackgroundCopyJob 介面

使用 [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) 介面將檔案新增至作業、設定作業的優先權層級、判斷作業的狀態，以及啟動和停止作業。

若要建立作業，請呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md) 方法。 若要取得現有作業的 [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) 介面指標，請呼叫 [**IBackgroundCopyManager：： GetJob**](ibackgroundcopymanager-getjob.md) 方法。

## <a name="members"></a>成員

**IBackgroundCopyJob** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IBackgroundCopyJob** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyJob** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取消**](ibackgroundcopyjob-cancel.md)                             | 取消作業，並從用戶端移除暫存檔案。<br/>                                                                                                                                                           |
| [**完成**](ibackgroundcopyjob-complete.md)                         | 結束作業，並將傳輸的檔案儲存在用戶端上。<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | 傳回列舉值物件的介面指標，您可以用來列舉作業中的檔案。<br/>                                                                                                                   |
| [**GetDisplayName**](ibackgroundcopyjob-getdisplayname.md)             | 抓取識別作業的顯示名稱。<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | 在發生錯誤之後，捕獲錯誤物件的介面指標。<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | 抓取佇列中作業的識別碼。<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | 抓取在遇到暫時性錯誤狀況之後，繼續嘗試傳送檔案的時間長度。<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | 抓取您為應用程式設定的事件通知 (回呼) 旗標。<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | 抓取 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面的實 (回呼) 的指標。<br/>                                                                                    |
| [**GetPriority**](ibackgroundcopyjob-getpriority.md)                   | 抓取您為作業設定的優先權層級。<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | 抓取作業相關的進度資訊，例如傳送至用戶端的位元組數和檔案數目。<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | 捕獲作業的狀態。<br/>                                                                                                                                                                                        |
| [**GetTimes**](ibackgroundcopyjob-gettimes.md)                         | 抓取與作業相關之活動的時間戳記，例如作業的建立時間。<br/>                                                                                                                         |
| [**GetType**](ibackgroundcopyjob-gettype.md)                           | 抓取正在執行的傳輸類型，例如檔案下載。<br/>                                                                                                                                               |
| [**繼續**](ibackgroundcopyjob-resume.md)                             | 開始新的作業，或重新開機已暫停的工作。<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | 指定在遇到暫時性錯誤狀況之後，繼續嘗試傳送檔案的時間長度。<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | 指定要接收的事件通知類型。<br/>                                                                                                                                                                   |
| [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)     | 指定 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面的實 (回呼) 的指標。 介面會根據您設定的事件通知旗標來接收通知。<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | 指定相對於傳送佇列中其他作業的作業優先順序。<br/>                                                                                                                                        |
| [**暫停**](ibackgroundcopyjob-suspend.md)                           | 暫停作業。<br/>                                                                                                                                                                                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

