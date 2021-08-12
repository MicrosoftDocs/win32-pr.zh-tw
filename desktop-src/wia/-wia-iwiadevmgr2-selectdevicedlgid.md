---
description: IWiaDevMgr2：： SelectDeviceDlgID 方法-顯示對話方塊，讓使用者選取硬體裝置以取得影像。
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'IWiaDevMgr2：： SelectDeviceDlgID 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 95b5134a2c7f7411ffcf2860f8829225a7271089c824b4e4c8731de78ffa4a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440800"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>IWiaDevMgr2：： SelectDeviceDlgID 方法

顯示對話方塊，讓使用者選取硬體裝置以取得影像。

## <a name="syntax"></a>語法


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

指定 [ **選取裝置** ] 對話方塊的父視窗。

</dd> <dt>

*lDeviceType* \[在\]
</dt> <dd>

類型： **LONG**

指定要使用的 WIA 2.0 裝置類型。 如需可能值的清單，請參閱 [WIA 裝置類型](-wia-wia-device-type-specifiers.md) 規範。

</dd> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定對話方塊的行為。 值可以是下列其中一項。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

使用預設行為。

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ 選取 \_ 裝置 \_ NODEFAULT**


</dt> <dd>

即使只有一個相符的裝置，仍顯示對話方塊。

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[退出，retval\]
</dt> <dd>

類型： **BSTR \***

接收裝置識別碼字串之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

這個方法可以傳回其中一個值。



| 傳回碼                                                                                                  | 描述                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 已成功選取裝置。 <br/>                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | 使用者已取消對話方塊。 <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ 沒有 \_ 任何 \_ 可用的裝置**</dt> </dl> | 沒有任何 WIA 2.0 硬體裝置符合 *lDeviceType* 參數中提供的規格。 <br/> |



 

## <a name="remarks"></a>備註

此方法會建立並顯示 [ **選取裝置** ] 對話方塊，讓使用者可以選取 WIA 2.0 裝置來取得影像。 如果成功選取裝置， **IWiaDevMgr2：： SelectDeviceDlgID** 方法會透過其 *pbstrDeviceID* 參數，將其識別碼字串傳遞至應用程式。

應用程式可以透過 *lDeviceType* 參數指定裝置類型，以將向使用者顯示的裝置限制為特定類型。 如果只有一部裝置符合規格， **IWiaDevMgr2：： SelectDeviceDlgID** 不會顯示 [ **選取裝置** ] 對話方塊。 相反地，它會將裝置的識別碼字串傳遞至應用程式，而不會顯示對話方塊。 您可以覆寫此行為，並強制 **IWiaDevMgr2：： SelectDeviceDlgID** 藉由傳遞 WIA \_ 選取 \_ 裝置 \_ NODEFAULT 作為 *lFlags* 參數的值來顯示對話方塊。 如果有一個以上的 WIA 2.0 裝置符合規格，則所有相符的裝置都會顯示在 [SelectDevice] 對話方塊中，讓使用者可以選擇其中一個。

> [!Note]  
> 建議應用程式 **在 [檔案**] 功能表上，透過 [掃描器]**中** 名稱為的功能表項目，讓裝置和影像可供選擇。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




