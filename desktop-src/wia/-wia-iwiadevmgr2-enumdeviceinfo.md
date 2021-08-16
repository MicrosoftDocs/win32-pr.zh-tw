---
description: 針對每個可用的 Windows 映像取得 (WIA) 2.0 裝置，建立屬性資訊的列舉值。
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2：： EnumDeviceInfo 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 8b646c494d9793986373d45db2d89dfde91e744196d86d28aceab35874f504d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208720"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>IWiaDevMgr2：： EnumDeviceInfo 方法

針對每個可用的 Windows 映像取得 (WIA) 2.0 裝置，建立屬性資訊的列舉值。

## <a name="syntax"></a>語法


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定要列舉的 WIA 2.0 裝置類型。

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ >LNK-DEVINFO \_ 列舉 \_ 區域**


</dt> <dd>

只會列舉在本機連線的主動式掃描器裝置。

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ >LNK-DEVINFO \_ 列舉 \_ 全部**


</dt> <dd>

所有裝置都會在本機和遠端列舉，包括非使用中 (中斷連線) 裝置和舊版 STI 裝置。

</dd> </dl> </dd> <dt>

*ppIEnum* \[退出，retval\]
</dt> <dd>

類型： **[ **IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

接收 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) 介面之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

**IWiaDevMgr2：： EnumDeviceInfo** 方法會建立支援 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面的列舉值物件。 方法會在參數 *ppIEnum* 中儲存 **IEnumWIA \_ DEV \_ INFO** 介面的指標。 應用程式可以使用 **IEnumWIA \_ DEV \_ INFO** 介面指標來列舉附加至使用者電腦的每個 WIA 2.0 裝置的屬性。

應用程式必須在透過 *ppIEnum* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
