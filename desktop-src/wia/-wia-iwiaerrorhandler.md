---
description: IWiaErrorHandler 介面會提供方法來處理應用程式要求影像資料時可能發生的錯誤（不論是預覽或最終位）。
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: 'IWiaErrorHandler 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6e97c5a146c23ce1ecdb2ba77cde5d37cd9091fc9d77e288042f02fc118816e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965587"
---
# <a name="iwiaerrorhandler-interface"></a>IWiaErrorHandler 介面

**IWiaErrorHandler** 介面會提供方法來處理應用程式要求影像資料時可能發生的錯誤（不論是預覽或最終位）。

## <a name="members"></a>成員

**IWiaErrorHandler** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaErrorHandler** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaErrorHandler** 介面具有這些方法。



| 方法                                                                     | 描述                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | 傳回描述狀態碼的字串。<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | 處理影像資料傳輸期間的狀態和錯誤訊息，並將其顯示給使用者。<br/> |



 

## <a name="remarks"></a>備註

應用程式回呼物件可以執行 **IWiaErrorHandler**。

此介面並非設計用來處理在影像資料傳輸之外發生的錯誤，例如，取得或設定裝置屬性或 unreturned 回呼至驅動程式時發生錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
