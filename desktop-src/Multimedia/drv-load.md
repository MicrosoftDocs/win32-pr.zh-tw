---
title: 'DRV_LOAD 訊息 (Mmsystem .h) '
description: 通知驅動程式已載入它。 驅動程式應該確保任何需要的硬體和支援驅動程式都存在。
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935073"
---
# <a name="drv_load-message"></a>WINSPOOL.DRV \_ 載入訊息

通知驅動程式已載入它。 驅動程式應該確保任何需要的硬體和支援驅動程式都存在。

## <a name="parameters"></a>參數

*Hdrvr* 參數一律為零。 不會使用 *dwDriverId*、 *lParam1* 和 *lParam2* 參數。

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

**Winspool.drv \_ 載入** 訊息一律是設備磁碟機所收到的第一則訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[可安裝的驅動程式](installable-drivers.md)
</dt> <dt>

[可安裝的驅動程式訊息](installable-driver-messages.md)
</dt> </dl>

 

 





