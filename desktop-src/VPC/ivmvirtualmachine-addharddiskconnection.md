---
title: 'IVMVirtualMachine AddHardDiskConnection 方法 (VPCCOMInterfaces .h) '
description: 將新的硬碟連接新增至虛擬機器。
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- AddHardDiskConnection 方法 Virtual PC
- AddHardDiskConnection 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AddHardDiskConnection 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967972"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>IVMVirtualMachine：： AddHardDiskConnection 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將新的硬碟連線新增到虛擬機器 (VM) 。

## <a name="syntax"></a>語法


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hardDiskPath* \[在\]
</dt> <dd>

要連接的虛擬硬碟 (VHD) 檔案的完整路徑。

</dd> <dt>

*busNumber* \[在\]
</dt> <dd>

將連接磁片磁碟機的匯流排。



| 值                                                                        | 意義                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 磁片磁碟機將會附加至第一個匯流排。<br/>  |
| <dl> <dt>1</dt> </dl> | 磁片磁碟機將會附加至第二個匯流排。<br/> |



 

</dd> <dt>

*deviceNumber* \[在\]
</dt> <dd>

將連接磁片磁碟機的裝置。



| 值                                                                        | 意義                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 磁片磁碟機將會連接到匯流排上的第一個裝置。<br/>  |
| <dl> <dt>1</dt> </dl> | 磁片磁碟機將會連接到匯流排上的第二個裝置。<br/> |



 

</dd> <dt>

*hardDiskConnection* \[退出，retval\]
</dt> <dd>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                              | Description                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                    | 作業成功。<br/>                                                                                                                  |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                      | *HardDiskConnection* 參數為 **Null**。<br/>                                                                                                |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | *HardDiskPath* 參數為 **Null** 或 *busNumber* 或 *deviceNumber* 參數無效。<br/>                                            |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt> </dl>   | 系統找不到 *hardDiskPath* 參數所指定的檔案。<br/>                                                                     |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt> </dl>   | 系統找不到 *hardDiskPath* 參數所指定的路徑。<br/>                                                                     |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>      | *HardDiskPath* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。<br/>                                                        |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>      | *HardDiskPath* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                                                |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl>   | *HardDiskPath* 參數所指定的路徑太長。 路徑必須少於260個字元。<br/>                                     |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                              | 未知的設定。<br/>                                                                                                                  |
| <dl> <dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt> </dl>                   | VM 處於執行中或已儲存狀態。<br/>                                                                                                         |
| <dl> <dt>**VM \_E \_ 磁片 \_ 磁碟機 \_ 匯流排 \_ \_ 使用中的 LOC**</dt> <dt>0xA00400503</dt> </dl>                | 指定的匯流排位置正在使用中。<br/>                                                                                                          |
| <dl> <dt>**VM \_E \_ 不正確 \_ HD \_ FILE**</dt> <dt>0xA0040682</dt> </dl>                        | VHD 超過 127 GB，因此無法連線至 IDE 匯流排。<br/>                                                                         |
| <dl> <dt>**VM \_E \_ 不支援的 \_ HD \_ 磁片 \_ 類型**</dt> <dt>0xA00400686</dt> </dl>             | *HardDiskPath* 參數會將連結的 vhd 或差異 vhd 參考至連結的 vhd。 連結的 Vhd 無法附加至虛擬機器。<br/> |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt> </dl> | 指定的 VHD 已連線到此 VM 的其他匯流排位置。<br/>                                                                    |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                              | 已發生未預期的錯誤。<br/>                                                                                                              |



 

## <a name="remarks"></a>備註

您只能將新的硬碟連接新增至已停止的虛擬機器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

