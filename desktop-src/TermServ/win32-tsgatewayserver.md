---
title: Win32_TSGatewayServer 類別
description: 用於遠端桌面閘道 (RD 閘道) 伺服器特定的作業。
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer 類別遠端桌面服務
- Win32_TSGatewayServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cd6c24447e7ba3bc22788484b2ac9e437ee947243c17a676728d2a336bd326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603882"
---
# <a name="win32_tsgatewayserver-class"></a>Win32 \_ TSGatewayServer 類別

用於遠端桌面閘道 (RD 閘道) 伺服器特定的作業。

## <a name="syntax"></a>語法

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayServer** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayServer** 類別具有這些方法。



| 方法                                                                                   | 描述                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | 使用指定的主體名稱建立自我簽署憑證，並將憑證雜湊傳回為 "out" 參數。<br/> |
| [**出口**](export-win32-tsgatewayserver.md)                                           | 以 XML 字串形式傳回 RD 閘道伺服器設定。<br/>                                                       |
| [**匯入**](import-win32-tsgatewayserver.md)                                           | 匯入指定的設定至 RD 閘道伺服器。<br/>                                                             |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

