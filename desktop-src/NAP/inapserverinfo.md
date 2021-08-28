---
title: 'INapServerInfo 介面 (NapServerManagement .h) '
description: 管理用戶端 (例如 WMI 提供者或命令列工具，) 用來查詢 NAP 伺服器系統的狀態。
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- INapServerInfo 介面 NAP
- INapServerInfo 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 556c2a5b7e7545038995d5091d46931352f9ee32bddfa31b91237dfa54d69620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626098"
---
# <a name="inapserverinfo-interface"></a>INapServerInfo 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapServerInfo** 提供管理用戶端 (的方法，例如 WMI 提供者或命令列工具，) 用來查詢 NAP 伺服器系統的狀態。

## <a name="members"></a>成員

**INapServerInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapServerInfo** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapServerInfo** 介面具有這些方法。



| 方法                                                                                                                   | 描述                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**INapServerInfo::GetFailureCategoryMappings**](inapserverinfo-getfailurecategorymappings-method.md)                   | 抓取指定 SHV 的失敗類別對應。<br/> |
| [**INapServerInfo::GetNapServerInfo**](inapserverinfo-getnapserverinfo-method.md)                                       | 抓取 NAP 伺服器的相關資訊。<br/>                  |
| [**INapServerInfo::GetRegisteredSystemHealthValidators**](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | 抓取已註冊的 Shv 清單。<br/>                         |



 

## <a name="remarks"></a>備註

這些方法只提供有關系統上 NAP 伺服器及其元件的靜態資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapServerManagement。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

