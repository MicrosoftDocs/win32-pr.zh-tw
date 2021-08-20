---
description: IWiaDevMgr：： GetImageDlg、IWiaDevMgr2：： GetImageDlg、IWiaItem：:D eviceDlg 和 IWiaItem2：:D eviceDlg 方法用來控制對話方塊作業的旗標。
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: 'WiaFlag (Wiadef) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: bfff3ccab0f8aa73c2ae6e34086c3abc909a4b4d8b9222bf4d6d8a86e0a36c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668961"
---
# <a name="wiaflag"></a>WiaFlag

[**IWiaDevMgr：： GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg)、 [**IWiaDevMgr2：： GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)、 [**IWiaItem：:D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)和 [**IWiaItem2：:D evicedlg**](-wia-iwiaitem2-devicedlg.md)方法用來控制對話方塊作業的旗標。



| 常數                                                                                                                                                                                                                | 描述                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**WIA \_ 裝置 \_ 對話方塊 \_ 單一 \_ 影像**</dt> </dl>     | 在 [裝置映射取得] 對話方塊中，將影像選取範圍限制為單一影像。<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI**</dt> </dl> | 使用系統 UI （如果有的話），而不是廠商提供的 UI。 如果系統 UI 無法使用，則會使用廠商 UI。 如果沒有可用的 UI，函數會傳回 E \_ >notimpl。<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA \_ 選取 \_ 裝置 \_ NODEFAULT**</dt> </dl>               | 強制 [**IWiaDevMgr：： GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) 或 [**IWiaDevMgr2：： GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) 方法顯示 [ **選取裝置** ] 對話方塊。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




