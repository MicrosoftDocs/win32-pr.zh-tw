---
title: 'INapComponentInfo 介面 (NapCommon .h) '
description: 提供外掛程式元件 (的方法，例如 Sha 和 Shv) 必須執行，NAP 系統才能與其通訊。
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- INapComponentInfo 介面 NAP
- INapComponentInfo 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188aae04ab407c5ae26e1d1a764e9093cc101cbe7d714ef8a8e0146013fefee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799703"
---
# <a name="inapcomponentinfo-interface"></a>INapComponentInfo 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentInfo** 介面提供外掛程式元件 (的方法，例如 Sha 和 shv，) 必須為 NAP 系統執行才能與它們進行通訊。 NAP 系統會呼叫這些方法的執行，以抓取靜態的系統管理資訊 (例如，易記名稱或當地語系化的字串) 。

## <a name="members"></a>成員

**INapComponentInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapComponentInfo** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapComponentInfo** 介面具有這些方法。



| 方法                                                                                                         | 描述                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | NAP 系統用來要求健康情況用戶端將 HRESULT 錯誤碼轉換成訊息識別碼。<br/> |
| [**INapComponentInfo：： GetDescription**](inapcomponentinfo-getdescription-method.md)                           | NAP 系統用來取得健全狀況用戶端的描述。<br/>                                  |
| [**INapComponentInfo::GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | NAP 系統用來取得健全狀況用戶端的易記名稱。<br/>                                |
| [**INapComponentInfo::GetIcon**](inapcomponentinfo-geticon-method.md)                                         | NAP 系統用來取得健全狀況用戶端的圖示。<br/>                                         |
| [**INapComponentInfo::GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | NAP 系統用來取得當地語系化的字串。<br/>                                                   |
| [**INapComponentInfo::GetVendorName**](inapcomponentinfo-getvendorname-method.md)                             | NAP 系統用來取得健康情況用戶端的廠商名稱。<br/>                                  |
| [**INapComponentInfo：： GetVersion**](inapcomponentinfo-getversion-method.md)                                   | NAP 系統用來取得健全狀況用戶端的版本。<br/>                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

