---
title: Win32_TSGeneralSetting 類別的 SetEncryptionLevel 方法 \(英文\)
description: SetEncryptionLevel 方法會設定加密層級。
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- SetEncryptionLevel 方法遠端桌面服務
- SetEncryptionLevel 方法遠端桌面服務，Win32_TSGeneralSetting 類別
- Win32_TSGeneralSetting 類別遠端桌面服務，SetEncryptionLevel 方法
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104597"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Win32 TSGeneralSetting 類別的 SetEncryptionLevel 方法 \_

**SetEncryptionLevel** 方法會設定加密層級。

## <a name="syntax"></a>語法


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MinEncryptionLevel* \[在\]
</dt> <dd>

要設定的最小加密層級。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

低層級的加密。 只有從用戶端傳送到伺服器的資料會使用56位加密進行加密。 請注意，從伺服器傳送到用戶端的資料並未加密。

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

用戶端相容的加密層級。 從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會以用戶端所支援的最大金鑰強度進行加密。

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

高層級的加密。 從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用強式128位加密進行加密。 無法連接不支援此加密層級的用戶端。

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**億**


</dt> <dd>

符合 FIPS 規範的加密。 從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用 Microsoft 密碼編譯模組，以聯邦資訊處理標準 (FIPS) 加密演算法進行加密和解密。 FIPS 是「密碼編譯模組的安全性需求」的標準。 FIPS 140-1 (1994) 和 FIPS 140-2 (2001) 描述美國政府內所使用之硬體和軟體密碼編譯模組的政府需求。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回成功，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> </dl>

 

