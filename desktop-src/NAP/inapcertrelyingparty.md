---
title: 'INapCertRelyingParty 介面 (NapCertRelyingParty .h) '
description: 憑證-信賴憑證者必須使用來與 NapAgent 通訊。
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- INapCertRelyingParty 介面 NAP
- INapCertRelyingParty 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d2a68c6ce910fa63588df1fa7bc1834f6ed537a2a2c9b85f24d383497a8d463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368607"
---
# <a name="inapcertrelyingparty-interface"></a>INapCertRelyingParty 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapCertRelyingParty** 介面提供憑證信賴憑證者必須用來與 NapAgent 進行通訊的方法。

## <a name="members"></a>成員

**INapCertRelyingParty** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapCertRelyingParty** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapCertRelyingParty** 介面具有這些方法。



| 方法                                                                                                        | 描述                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**INapCertRelyingParty::GetSubscribedRelyingParties**](inapcertrelyingparty-getsubscribedrelyingparties.md) | 取得已訂閱的信賴憑證者清單。<br/>                 |
| [**INapCertRelyingParty::SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)               | 訂閱已註冊的健康情況憑證伺服器 (HCS) 。<br/> |
| [**INapCertRelyingParty::UnSubscribeCertByGroup**](inapcertrelyingparty-unsubscribecertbygroup.md)           | 從 HCS 伺服器取消訂閱。<br/>                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapCertRelyingParty。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCertRelyingParty .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

