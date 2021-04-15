---
description: 提供可取代預設系統使用者介面的自訂使用者介面。
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
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511625"
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

類型： **PDEVICEDIALOGDATA \** _

指向 [_ *DEVICEDIALOGDATA* *](-wia-devicedialogdata.md)結構，其中包含執行裝置對話方塊所需的所有資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果方法成功，它會傳回 S \_ OK。 如果使用者取消對話方塊，則此方法會傳回 \_ FALSE。 如果未執行此方法，則會傳回 E \_ >notimpl。 如果方法失敗，則會傳回標準 COM 錯誤碼。

## <a name="remarks"></a>備註

如果您執行 [**IWiaUIExtension**](-wia-iwiauiextension.md) 介面，但不想取代系統使用者介面，則必須執行此方法，但它應該不會執行任何比傳回 E >notimpl 還多的動作 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl> |



 

 




