---
title: 'IVMVirtualPC RemoveConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 移除指定之設定的值。
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- RemoveConfigurationValue 方法 Virtual PC
- RemoveConfigurationValue 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，RemoveConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844052"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a>IVMVirtualPC：： RemoveConfigurationValue 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

移除指定之設定的值。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*preferenceKey* \[在\]
</dt> <dd>

用來識別喜好設定的金鑰，儲存在設定檔中。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                              | 作業成功。<br/>                                                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                | *PreferenceKey* 參數為 **Null**。<br/>                                           |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | *PreferenceKey* 參數無效或為空字串。<br/>                    |
| <dl> <dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt> </dl>                   | 找不到喜好設定。<br/>                                                        |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl> | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                        | 已發生未預期的錯誤。<br/>                                                    |



 

## <a name="remarks"></a>備註

這個方法可為目前使用者的任何喜好設定值提供低層級的存取權。 可以用來移除客戶定義索引鍵的喜好設定值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

