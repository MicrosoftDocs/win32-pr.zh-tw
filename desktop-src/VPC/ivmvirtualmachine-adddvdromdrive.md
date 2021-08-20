---
title: 'IVMVirtualMachine AddDVDROMDrive 方法 (VPCCOMInterfaces .h) '
description: 將新的 CD 或 DVD 光碟機新增至虛擬機器。
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVDROMDrive 方法 Virtual PC
- AddDVDROMDrive 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AddDVDROMDrive 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a875af50d38270b898c17f2848a4e4b33fe79a4b17d9ab7b6be58cdcfcf92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123228"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>IVMVirtualMachine：： AddDVDROMDrive 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將新的 CD 或 DVD 光碟機新增至虛擬機器。

## <a name="syntax"></a>語法


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

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

*dvdDrive* \[退出，retval\]
</dt> <dd>

[**IVMDVDDrive**](ivmdvddrive.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                               | 描述                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                     | 作業成功。<br/>                       |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                       | *DvdDrive* 參數為 **Null**。<br/>               |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | 參數無效。<br/>                           |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>               | 未知的設定。<br/>                       |
| <dl> <dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt> </dl>    | 虛擬機器處於執行中或已儲存狀態。<br/> |
| <dl> <dt>**VM \_E \_ 磁片 \_ 磁碟機 \_ 匯流排 \_ \_ 使用中的 LOC**</dt> <dt>0xA00400503</dt> </dl> | 指定的匯流排位置正在使用中。<br/>               |
| <dl> <dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt> </dl>            | 指定的磁片磁碟機無效。<br/>                   |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>               | 已發生未預期的錯誤。<br/>                   |



 

## <a name="remarks"></a>備註

您只能將新的 CD 或 DVD 光碟機新增至已停止的虛擬機器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

