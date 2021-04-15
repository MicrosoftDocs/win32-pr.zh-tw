---
title: 'INapServerCallback 介面 (NapSystemHealthValidator .h) '
description: Shv 用來發出非同步要求完成的信號。
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- INapServerCallback 介面 NAP
- INapServerCallback 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464341"
---
# <a name="inapservercallback-interface"></a>INapServerCallback 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapServerCallback** 會提供一種方法，讓 shv 用來指示非同步要求完成。

## <a name="members"></a>成員

**INapServerCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapServerCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapServerCallback** 介面具有這些方法。



| 方法                                                                         | 描述                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapServerCallback：： OnComplete**](inapservercallback-oncomplete-method.md) | 由 Shv 用來指示非同步要求完成。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

