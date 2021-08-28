---
description: IWiaUIExtension：:D eviceDialog 方法-提供可取代預設系統使用者介面的自訂使用者介面。
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: 'IWiaUIExtension：:D eviceDialog 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: a06ac5428743c31bae22c6d106ee927791739295754b15ac9764045c3aeeffab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813868"
---
# <a name="iwiauiextensiondevicedialog-method"></a>IWiaUIExtension：:D eviceDialog 方法

提供可取代預設系統使用者介面的自訂使用者介面。

## <a name="syntax"></a>語法


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDeviceDialogData* \[在\]
</dt> <dd>

類型： **PDEVICEDIALOGDATA \***

指向 [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) 結構，其中包含執行裝置對話方塊所需的所有資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果方法成功，它會傳回 S \_ OK。 如果使用者取消對話方塊，則此方法會傳回 \_ FALSE。 如果未執行此方法，則會傳回 E \_ >notimpl。 如果方法失敗，則會傳回標準 COM 錯誤碼。

## <a name="remarks"></a>備註

如果您執行 [**IWiaUIExtension**](-wia-iwiauiextension.md) 介面，但不想取代系統使用者介面，則必須執行此方法，但它應該不會執行任何比傳回 E >notimpl 還多的動作 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl> |



 

 




