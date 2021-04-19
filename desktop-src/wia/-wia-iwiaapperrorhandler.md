---
description: IWiaAppErrorHandler 介面可讓應用程式在資料傳輸期間顯示錯誤的 windows () 使用者可以從中選擇是否要繼續、取消或中止傳送。
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: 'IWiaAppErrorHandler 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971807"
---
# <a name="iwiaapperrorhandler-interface"></a>IWiaAppErrorHandler 介面

**IWiaAppErrorHandler** 介面可讓應用程式在資料傳輸期間顯示錯誤的 windows () 使用者可以從中選擇是否要繼續、取消或中止傳送。

## <a name="members"></a>成員

**IWiaAppErrorHandler** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaAppErrorHandler** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaAppErrorHandler** 介面具有這些方法。



| 方法                                                        | 描述                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | 取得對話方塊的控制碼，此控制碼會顯示錯誤訊息，並提供一或多個按鈕來繼續、取消或中止應用程式。<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | 處理影像資料傳輸期間的裝置狀態和錯誤訊息，並向使用者顯示訊息。<br/>                                  |



 

## <a name="remarks"></a>備註

處理此介面的錯誤處理（或回呼）物件會傳遞至 [**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md) 和 [**IWiaTransfer：： Upload**](-wia-iwiatransfer-upload.md)。

此介面並非設計用來處理在影像資料傳輸之外發生的錯誤，例如，取得或設定裝置屬性或 unreturned 回呼至驅動程式時發生錯誤。

驅動程式錯誤處理常式應該執行 [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)，而不是 **IWiaAppErrorHandler**。

執行這個介面的物件也應該執行 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)。

如果您想要驅動程式錯誤處理常式和預設錯誤處理常式來顯示錯誤訊息視窗，但您不想要為應用程式建立完整的錯誤處理常式，請執行這個介面，並同時執行 [**IWiaAppErrorHandler：： ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) 方法，以傳回 \_ 未處理的 WIA 狀態 \_ \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
