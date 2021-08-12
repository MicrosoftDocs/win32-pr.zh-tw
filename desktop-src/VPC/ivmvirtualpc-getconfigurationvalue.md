---
title: 'IVMVirtualPC GetConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 擷取指定之組態設定的值。
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- GetConfigurationValue 方法 Virtual PC
- GetConfigurationValue 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a483211353474f3328fc4e5da3b80ecf3fbbece53bc306e546f85543ac9027e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591859"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>IVMVirtualPC：： GetConfigurationValue 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

擷取指定之組態設定的值。

## <a name="syntax"></a>語法


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*preferenceKey* \[在\]
</dt> <dd>

用來識別喜好設定的金鑰，儲存在設定檔中。

</dd> <dt>

*preferenceValue* \[退出，retval\]
</dt> <dd>

喜好設定值。 這個參數可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ I4** (整數) 或 **vt \_ BOOL** (布林值) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                        | 描述                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                              | 作業成功。<br/>                                                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                | *PreferenceKey* 或 *PreferenceValue* 參數為 **Null**。<br/>                      |
| <dl> <dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xa0040300</dt> </dl>                   | 找不到喜好設定。<br/>                                                        |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl> | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                        | 已發生未預期的錯誤。<br/>                                                    |



 

## <a name="remarks"></a>備註

這個方法可為目前使用者的任何喜好設定值提供低層級的存取權。 您可以使用它來抓取客戶定義索引鍵的喜好設定值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

