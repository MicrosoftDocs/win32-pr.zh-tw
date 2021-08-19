---
title: 'INapSoHConstructor 介面 (NapProtocol .h) '
description: Sha 用來建立 SoHRequests，以及由 Shv 用來建立 SoHResponses。
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- INapSoHConstructor 介面 NAP
- INapSoHConstructor 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ceb9e927e1ac65f21a3ff457922e1bd475b8327ac2525b2af7afefa6cb173f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037848"
---
# <a name="inapsohconstructor-interface"></a>INapSoHConstructor 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHConstructor** 會提供方法，讓 sha 用來建立 [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) ，並由 Shv 用來建立 **SoHResponses**。

## <a name="members"></a>成員

**INapSoHConstructor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapSoHConstructor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSoHConstructor** 介面具有這些方法。



| 方法                                                                                   | 描述                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor::AppendAttribute**](inapsohconstructor-appendattribute-method.md) | 將 TLV 新增至 SoH 緩衝區的結尾。<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | 抓取已建造的 SoH 封包。<br/>    |
| [**INapSoHConstructor：： Initialize**](inapsohconstructor-initialize-method.md)           | 初始化 SoH 封包。<br/>              |
| [**INapSoHConstructor：： Validate**](inapsohconstructor-validate-method.md)               | 檢查 SoH 封包的有效性。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

