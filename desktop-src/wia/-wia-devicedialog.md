---
description: 由應用程式用來向使用者顯示裝置對話方塊。
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: 'DeviceDialog 函式 (Wiadevd) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982438"
---
# <a name="devicedialog-function"></a>DeviceDialog 函式

由應用程式用來向使用者顯示裝置對話方塊。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDeviceDialogData* \[在\]
</dt> <dd>

類型： **PDEVICEDIALOGDATA**

用來建立裝置對話方塊的 [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




