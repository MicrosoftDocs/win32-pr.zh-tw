---
title: 'IVMVirtualPC RegisterVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 註冊現有的虛擬機器設定，並抓取虛擬機器物件。
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- RegisterVirtualMachine 方法 Virtual PC
- RegisterVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，RegisterVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3752b613bb3adc97d1e0968d989b5c97c616b76883ef89880be7c00d720c62a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998530"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a>IVMVirtualPC：： RegisterVirtualMachine 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

註冊現有的虛擬機器設定，並抓取虛擬機器物件。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*configurationName* \[在\]
</dt> <dd>

要註冊之虛擬機器的名稱。 名稱的長度不能超過80個字元，且名稱和路徑的加總長度不能超過 **最大 \_ 路徑** (260) 個字元。 指定的名稱可能包含 .vmc 延伸模組。 如果此參數為 **Null** 或空字串，則 *configurationPath* 參數必須指定設定檔案的完整路徑。

</dd> <dt>

*configurationPath* \[在\]
</dt> <dd>

包含現有設定檔案的資料夾路徑。 如果 *configurationName* 參數為 **Null** 或空字串，則必須指定現有設定檔案的完整路徑。

</dd> <dt>

*virtualMachine* \[退出，retval\]
</dt> <dd>

代表此虛擬機器的新 [**IVMVirtualMachine**](ivmvirtualmachine.md) 物件指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                                                                                                          |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | *ConfigurationName* 或 *configurationPath* 參數無效，或 *virtualMachine* 為 **Null**。<br/>                                                                                                  |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt> </dl> | 系統找不到 *configurationName* 和 *configurationPath* 參數所指定的路徑。<br/>                                                                                               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt> </dl> | 系統找不到 *configurationName* 和 *configurationPath* 參數所指定的檔案。<br/>                                                                                               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>    | *ConfigurationPath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>    | 參數 *configurationPath* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                                                                                         |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl> | *ConfigurationName* 和 *configurationPath* 參數所指定的路徑會導致路徑太長。 路徑的加總長度必須小於 **最大 \_ 路徑** (260) 個字元。<br/> |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt> </dl>  | 此位置已有同名的設定檔。<br/>                                                                                                                                   |
| <dl> <dt>**VM \_E \_ CONFIG \_ NAME \_ 太 \_ 長**</dt> <dt>0xA0040401</dt> </dl>                | *ConfigurationName* 參數的長度超過80個字元。<br/>                                                                                                                                     |
| <dl> <dt>**VM \_E \_ CONFIG \_ NAME \_ 不正確 \_ CHAR**</dt> <dt>0xA0040402</dt> </dl>            | *ConfigurationName* 參數包含不正確字元 (" \* ？： <>/ \| \\ " ") 之一。<br/>                                                                                                         |
| <dl> <dt>**VM \_E \_ 設定 \_ 重複 \_ 名稱**</dt> <dt>0xA0040403</dt> </dl>                | 已經有虛擬機器使用此名稱。<br/>                                                                                                                                                     |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl>     | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/>                                                                                                                   |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                                                                                                      |



 

## <a name="remarks"></a>備註

虛擬機器名稱不區分大小寫，例如 "MyVM" 和 "MyVM" 指的是相同的虛擬機器。

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

 

