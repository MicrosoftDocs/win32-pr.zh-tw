---
title: 'IBackgroundCopyJob5 介面 (>deliveryoptimization .h) '
description: 您可以使用此介面來查詢或設定工作的數個選擇性行為。
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- IBackgroundCopyJob5 介面
- IBackgroundCopyJob5 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105324"
---
# <a name="ibackgroundcopyjob5-interface"></a>IBackgroundCopyJob5 介面

您可以使用此介面來查詢或設定工作的數個選擇性行為。

若要取得這個介面，請使用做為介面識別碼來呼叫 **IBackgroundCopyJob：： QueryInterface** 方法 `__uuidof(IBackgroundCopyJob5)` 。

## <a name="members"></a>成員

**IBackgroundCopyJob5** 介面繼承自 [**IBackgroundCopyJob**](ibackgroundcopyjob-.md)。 **IBackgroundCopyJob5** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyJob5** 介面具有這些方法。



| 方法                                                 | 描述                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | 用來取得作業屬性的泛型方法。<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | 設定 DO 作業屬性的泛型方法。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 定義為 E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





