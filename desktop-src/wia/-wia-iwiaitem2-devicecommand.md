---
description: 發出命令給 Windows 映像取得 (WIA) 2.0 硬體裝置。
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: 'IWiaItem2：:D eviceCommand 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972050"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2：:D eviceCommand 方法

發出命令給 Windows 映像取得 (WIA) 2.0 硬體裝置。

## <a name="syntax"></a>語法


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*pCmdGUID* \[在\]
</dt> <dd>

類型： **CONST GUID \** _

指定要傳送至 WIA 2.0 裝置的命令。 請參閱 [_ *WIA 裝置命令* *](-wia-wia-device-commands.md)。

</dd> <dt>

*ppIWiaItem2* \[in、out\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

接收命令所建立之 [**IWiaItem2**](-wia-iwiaitem2.md) 專案的指標位址（如果有的話）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

除了標準 COM 錯誤碼之外，此方法可能會傳回下列值。



| 傳回碼                                                                                       | Description                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ CMDNOTSUPPORTED**</dt> </dl> | 此命令不會針對呼叫方法的 [**IWiaItem2**](-wia-iwiaitem2.md) 介面來執行。 尚未定義此錯誤的數值。 <br/> |



 

## <a name="remarks"></a>備註

這個方法的行為會根據呼叫方法的節點類別而有所不同。

當應用程式使用 **IWiaItem2：:D evicecommand** 方法來傳送 [**WIA \_ CMD \_ TAKE \_ PICTURE**](-wia-wia-device-commands.md)命令至裝置時，WIA 2.0 執行時間系統會建立 [**IWiaItem2**](-wia-iwiaitem2.md)物件來代表影像。 **IWiaItem2：:D evicecommand** 方法會將介面的位址儲存在 *ppIWiaItem2* 參數中。

應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
