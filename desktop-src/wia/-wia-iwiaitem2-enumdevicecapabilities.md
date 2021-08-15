---
description: 建立用來確定命令和事件的列舉值， (WIA) 2.0 裝置支援的 Windows 映像。
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2：： EnumDeviceCapabilities 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6748966beaa3bf16f668c4b8b0de60a4302ebcf514f06a3d588999d5faebaf3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450458"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>IWiaItem2：： EnumDeviceCapabilities 方法

建立用來確定命令和事件的列舉值， (WIA) 2.0 裝置支援的 Windows 映像。

## <a name="syntax"></a>語法


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定旗標，以選取要列舉的功能類型。 這是下列其中一個值。

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA \_ 裝置 \_ 命令**


</dt> <dd>

列舉裝置命令。

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA \_ 裝置 \_ 事件**


</dt> <dd>

列舉裝置事件。

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_開發人員 \_ 帽* \[ 出\]
</dt> <dd>

類型： **[ **IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

接收這個方法所建立的 [**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法是用來建立列舉值物件，以取得 WIA 2.0 裝置支援的一組命令和事件。 *LFlags* 參數是用來指定要列舉哪些種類的裝置功能。 **IWiaItem2：： EnumDeviceCapabilities** 方法會在 *ppIEnumWIA \_ DEV \_ CAPS* 參數中儲存列舉值物件的介面位址。

此方法只能在裝置樹狀結構之 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的根項目上呼叫。

應用程式必須在透過 *ppIEnumWIA \_ DEV \_ cap* 參數所收到的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
