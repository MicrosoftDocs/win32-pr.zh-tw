---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 SetPortNumbers 方法
description: 設定允許透過遠端桌面閘道 (RD 閘道) 連接到資源的埠號碼。
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- SetPortNumbers 方法遠端桌面服務
- SetPortNumbers 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，SetPortNumbers 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c151302abfda0b6bc42566770c0e8b8fb10dbab789cf2ece886be557efb023e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987768"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Win32 TSGatewayResourceAuthorizationPolicy 類別的 SetPortNumbers 方法 \_

設定允許透過遠端桌面閘道 (RD 閘道) 連接到資源的埠號碼。

## <a name="syntax"></a>語法


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PortNumbers* \[在\]
</dt> <dd>

此遠端桌面資源授權原則允許的以分號分隔的埠號碼清單， (RD RAP) 。 若要允許任何埠號碼，請設定 " \* "。

</dd> </dl>

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

