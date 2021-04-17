---
title: 'IConnectionBrokerClient 介面 (Cbclient .h) '
description: 提供使用遠端桌面連線代理人用戶端所需的方法。
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- IConnectionBrokerClient 介面遠端桌面服務
- IConnectionBrokerClient 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466757"
---
# <a name="iconnectionbrokerclient-interface"></a>IConnectionBrokerClient 介面

提供使用遠端桌面連線代理人用戶端所需的方法。

此介面是由系統所執行。 若要取得這個介面的實例，請使用 [**CBCreateClientInstance**](cbcreateclientinstance.md) 函數。

## <a name="members"></a>成員

**IConnectionBrokerClient** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IConnectionBrokerClient** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IConnectionBrokerClient** 介面具有這些方法。



| 方法                                                         | 描述                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) | 要求應重新導向連接之目的電腦的相關資訊。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                       |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Cbclient。h</dt> </dl>      |
| 程式庫<br/>                  | <dl> <dt>Cbclient .lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IConnectionBrokerClient 定義為 D6818DF2-8338-4EB7-AD77-DE210817987C<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBCreateClientInstance**](cbcreateclientinstance.md)
</dt> </dl>

 

