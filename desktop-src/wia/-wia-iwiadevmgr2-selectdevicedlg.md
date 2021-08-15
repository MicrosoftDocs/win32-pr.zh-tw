---
description: IWiaDevMgr2：： SelectDeviceDlg 方法-顯示對話方塊，讓使用者選取硬體裝置以取得影像。
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'IWiaDevMgr2：： SelectDeviceDlg 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 344b13ec05e6f1d06011b3555e5b455202e5848b5000e799540d9f7c3160653b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441233"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>IWiaDevMgr2：： SelectDeviceDlg 方法

顯示對話方塊，讓使用者選取硬體裝置以取得影像。

## <a name="syntax"></a>語法


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
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

*pbstrDeviceID* \[in、out\]
</dt> <dd>

類型： **BSTR \***

在輸出時，會接收包含裝置識別碼字串的字串。 在輸入時，如果需要這項資訊，請傳遞指標的位址，如果不需要，則傳遞 **Null** 。

</dd> <dt>

*ppItemRoot* \[退出，retval\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

接收階層樹狀結構的根項目之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標位址，此介面表示所選的 WIA 2.0 裝置。 如果找不到任何裝置，則會收到 **Null**。

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

此方法會建立並顯示 [ **選取裝置** ] 對話方塊，讓使用者可以選取 WIA 2.0 裝置來取得影像。 如果成功選取裝置， **IWiaDevMgr2：： SelectDeviceDlg** 方法會為裝置建立 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。 它會在參數 *ppItemRoot* 中儲存根項目之 **IWiaItem2** 介面的指標。

應用程式可以透過 *lDeviceType* 參數指定裝置類型，以將向使用者顯示的裝置限制為特定類型。 如果只有一部裝置符合規格， **IWiaDevMgr2：： SelectDeviceDlg** 不會顯示 [ **選取裝置** ] 對話方塊。 相反地，它會建立裝置的 [**IWiaItem2**](-wia-iwiaitem2.md)樹狀結構，並在參數 *ppItemRoot* 中儲存根項目的 **IWiaItem2** 介面指標。 您可以覆寫此行為，並強制 **IWiaDevMgr2：： SelectDeviceDlg** 藉由指定 WIA \_ SELECT \_ DEVICE \_ NODEFAULT 作為 *lFlags* 參數的值來顯示對話方塊。 如果有一個以上的 WIA 2.0 裝置符合規格，則所有相符的裝置都會顯示在 [ **選取裝置** ] 對話方塊中，讓使用者可以選擇其中一個。

應用程式必須在透過 *ppItemRoot* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

> [!Note]  
> 建議應用程式 **在 [檔案**] 功能表上，透過 [掃描器]**中** 名稱為的功能表項目，讓裝置和影像可供選擇。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
