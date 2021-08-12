---
title: Win32_TSApplicationFileExtensions 類別的 FileExtensions 方法
description: 提供應用程式所處理的副檔名清單。
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- FileExtensions 方法遠端桌面服務
- FileExtensions 方法遠端桌面服務，Win32_TSApplicationFileExtensions 類別
- Win32_TSApplicationFileExtensions 類別遠端桌面服務，FileExtensions 方法
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c7c44acd410566c4f048cdf36bac904c18b21df42f53543051e3b94f49bfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609370"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Win32 TSApplicationFileExtensions 類別的 FileExtensions 方法 \_

提供應用程式所處理的副檔名清單。

## <a name="syntax"></a>語法


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppPath* \[在\]
</dt> <dd>

應用程式的路徑。

</dd> <dt>

*擴充* \[ 功能擴展\]
</dt> <dd>

應用程式所處理的副檔名。

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

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

