---
title: 'IBackgroundCopyError 介面 (>deliveryoptimization .h) '
description: 使用 IBackgroundCopyError 介面判斷錯誤的原因，以及傳輸程式是否可繼續。
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- IBackgroundCopyError 介面
- IBackgroundCopyError 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465077"
---
# <a name="ibackgroundcopyerror-interface"></a>IBackgroundCopyError 介面

使用 **IBackgroundCopyError** 介面判斷錯誤的原因，以及傳輸程式是否可繼續。

只有當工作的狀態是 BG_JOB_STATE_ERROR 或 BG_JOB_STATE_TRANSIENT_ERROR 時，才會建立錯誤物件。 當 **IBackgroundCopyXXXX** 介面方法失敗時，請勿建立 error 物件。 在開始傳輸資料 (工作的狀態變更為 BG_JOB_STATE_TRANSFERRING) 時，就可以使用 error 物件。

若要取得 **IBackgroundCopyError** 物件，請呼叫 [**IBackgroundCopyJob：： GetError**](ibackgroundcopyjob-geterror.md) 方法。

## <a name="members"></a>成員

**IBackgroundCopyError** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IBackgroundCopyError** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyError** 介面具有這些方法。



| 方法                                                   | 描述                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | 捕獲錯誤碼，並識別發生錯誤的內容。<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | 捕獲與錯誤相關聯之檔案物件的介面指標。<br/>     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError 定義為19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

