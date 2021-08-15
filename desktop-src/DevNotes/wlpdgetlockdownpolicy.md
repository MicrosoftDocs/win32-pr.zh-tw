---
description: 呼叫程式庫以取得相對於主機的安全性狀態，以及要使用的腳本或 msi。
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: 'WldpGetLockdownPolicy 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 47ae90c966ac259791d0ffb9c60d736430ede610db3932dd08ff60cc9e3b7b21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390188"
---
# <a name="wldpgetlockdownpolicy-function"></a>WldpGetLockdownPolicy 函式

呼叫程式庫以取得相對於主機的安全性狀態，以及要使用的腳本或 msi。 函數沒有相關聯的匯入程式庫。 您必須使用 LoadLibrary 和 GetProcAddress 函數，以動態方式連結至 wldp.dll。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hostInformation* \[在中，選擇性\]
</dt> <dd>

[**WLDP \_ 主機 \_ 資訊**](wldp-host-information.md)結構，用來識別要評估的主機和來源檔案。

</dd> <dt>

*lockdownState* \[擴展\]
</dt> <dd>

提供產生的原則安全值。 如果！WLDP_LOCKDOWN_IS_OFF，則會啟用 UMCI。 您也可以檢查 WLDP_LOCKDOWN_IS_AUDIT 和 WLDP_LOCKDOWN_IS_ENFORCE，以判斷原則是否處於 AUDIT 或強制模式。
</dd> <dt>

*lockdownFlags* \[在\]
</dt> <dd>

下列旗標值是定義 WLDP \_ FLAGS \_ SKIPSIGNATUREVALIDATION 0x00000100 –設定時，略過 SaferIdentifyLevel 驗證，這會忽略腳本是否經過簽署。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則此方法會傳回，否則會傳回 \_ 失敗碼。

## <a name="remarks"></a>備註

使用 WLDP \_ 主機 \_ 資訊來呼叫時。 SZSOURCE = Null，會傳回主機的一般原則。

使用 WLDP \_ 主機資訊呼叫時 \_ 。 DWHOSTID = WLDP \_ 主機 \_ 識別碼 \_ GLOBAL，WLDP \_ 主機 \_ 資訊。 szSource 必須是 Null，且函式會傳回全域系統原則。

您 \_ 可以使用 >DWFLAG WLDP 旗標 \_ SKIPSIGNATUREVALIDATION 來略過 SaferIdentifyLevel () 驗證，這會忽略腳本是否經過簽署。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




