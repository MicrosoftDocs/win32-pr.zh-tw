---
description: 為 Windows 映像取得 (WIA) 2.0 裝置建立 IWiaItem2 物件的階層式樹狀結構。
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2：： CreateDevice 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849358"
---
# <a name="iwiadevmgr2createdevice-method"></a>IWiaDevMgr2：： CreateDevice 方法

為 Windows 映像取得 (WIA) 2.0 裝置建立 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。

## <a name="syntax"></a>語法


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

指定 WIA 2.0 裝置的唯一識別碼。

</dd> <dt>

*ppWiaItem2Root* \[擴展\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

接收指向 WIA 2.0 裝置之階層樹狀結構中根項目之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

應用程式會使用 **IWiaDevMgr2：： CreateDevice** 方法，為 bstrDeviceID 參數所指定的 WIA 2.0 裝置建立裝置物件。 當它傳回時， **IWiaDevMgr2：： CreateDevice** 方法會將指標的位址儲存在參數 *ppWiaItem2Root* 中，指向 **IWiaDevMgr2：： CreateDevice** 所建立 [**IWiaItem2**](-wia-iwiaitem2.md)物件樹狀結構的根專案。 應用程式可以使用此物件樹狀結構來控制及取出 WIA 2.0 裝置的資料。

應用程式必須在透過 *ppWiaItem2Root* 參數接收的指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
