---
title: Win32_TSExpandEnvironmentVariables 類別的 EnvironmentVariables 方法
description: 展開系統定義的環境變數。 |Win32_TSExpandEnvironmentVariables 類別的 EnvironmentVariables 方法
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- EnvironmentVariables 方法遠端桌面服務
- EnvironmentVariables 方法遠端桌面服務，Win32_TSExpandEnvironmentVariables 類別
- Win32_TSExpandEnvironmentVariables 類別遠端桌面服務，EnvironmentVariables 方法
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49416291293d621739ab7c721ca349f5d87bb4582d1289f431a8c443d3414da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353890"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Win32 TSExpandEnvironmentVariables 類別的 EnvironmentVariables 方法 \_

展開系統定義的環境變數。

## <a name="syntax"></a>語法


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OriginalString* \[在\]
</dt> <dd>

包含要展開之環境變數的字串。

</dd> <dt>

*ExpandedString* \[擴展\]
</dt> <dd>

已展開環境變數的字串。

</dd> </dl>

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSExpandEnvironmentVariables**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

