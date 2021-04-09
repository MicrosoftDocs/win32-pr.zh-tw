---
description: IWiaDevMgr2 介面是用來建立及管理影像取得裝置，並註冊以接收裝置事件。
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: 'IWiaDevMgr2 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849355"
---
# <a name="iwiadevmgr2-interface"></a>IWiaDevMgr2 介面

**IWiaDevMgr2** 介面是用來建立及管理影像取得裝置，並註冊以接收裝置事件。

## <a name="members"></a>成員

**IWiaDevMgr2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaDevMgr2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaDevMgr2** 介面具有這些方法。



| 方法                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDevice**](-wia-iwiadevmgr2-createdevice.md)                                     | 針對 WIA 2.0 裝置建立 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。 <br/>                                                                                                                                                                                                                                                                                                 |
| [**EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | 針對每個可用的 WIA 2.0 裝置建立屬性資訊的列舉值。 <br/>                                                                                                                                                                                                                                                                                                                 |
| [**GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)                                       | [**IWiaDevMgr2：： GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)方法會顯示一或多個對話方塊，讓使用者從 WIA 2.0 裝置取得影像，並將影像寫入指定的檔案。 這個方法會擴充 [**IWiaDevMgr2：： SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) 的功能，以在單一 API 呼叫中封裝取得影像。 <br/> |
| [**RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | [**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)方法會註冊應用程式以接收事件，即使應用程式並未執行也一樣。<br/>                                                                                                                                                                                                      |
| [**RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) | 註冊 WIA 2.0 事件通知的執行中應用程式。 <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | [**IWiaDevMgr2：： RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)方法會註冊應用程式以接收裝置事件。 它主要是為了提供與未針對 WIA 2.0 撰寫之應用程式的回溯相容性。<br/>                                                                                                                         |
| [**SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md)                               | 顯示對話方塊，讓使用者選取硬體裝置以取得影像。 <br/>                                                                                                                                                                                                                                                                                                   |
| [**SelectDeviceDlgID**](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | 顯示對話方塊，讓使用者選取硬體裝置以取得影像。 <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>備註

**IWiaDevMgr2** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。



| IUnknown 方法                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
