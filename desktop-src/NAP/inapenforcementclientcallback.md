---
title: 'INapEnforcementClientCallback 介面 (NapEnforcementClient .h) '
description: 強制用戶端必須實行，才能讓 NapAgent 與其通訊。
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- INapEnforcementClientCallback 介面 NAP
- INapEnforcementClientCallback 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965121"
---
# <a name="inapenforcementclientcallback-interface"></a>INapEnforcementClientCallback 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientCallback** 介面提供強制用戶端必須執行的回呼方法，才能讓 NapAgent 與它們進行通訊。

## <a name="members"></a>成員

**INapEnforcementClientCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapEnforcementClientCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapEnforcementClientCallback** 介面具有這些方法。



| 方法                                                                                                         | 描述                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientCallback::GetConnections**](inapenforcementclientcallback-getconnections-method.md)   | 供 NapAgent 用來取出連接。<br/>                         |
| [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) | NapAgent 用來通知強制用戶端有 SoH 變更。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |



 

