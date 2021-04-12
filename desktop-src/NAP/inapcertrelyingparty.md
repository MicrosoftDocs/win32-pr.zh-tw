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
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025267"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapCertRelyingParty。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

