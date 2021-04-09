---
title: 'IBackgroundCopyManager 介面 (>deliveryoptimization .h) '
description: 建立傳送作業、抓取包含佇列中之作業的列舉值物件，以及從佇列中取出個別的作業。
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- IBackgroundCopyManager 介面
- IBackgroundCopyManager 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934498"
---
# <a name="ibackgroundcopymanager-interface"></a>IBackgroundCopyManager 介面

建立傳送作業、抓取包含佇列中之作業的列舉值物件，以及從佇列中取出個別的作業。

## <a name="members"></a>成員

**IBackgroundCopyManager** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IBackgroundCopyManager** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyManager** 介面具有這些方法。



| 方法                                                | 描述                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**>batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md) | 建立傳送工作。<br/>                   |
| [**GetJob**](ibackgroundcopymanager-getjob.md)       | 從佇列中取出指定的工作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager 定義為5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

