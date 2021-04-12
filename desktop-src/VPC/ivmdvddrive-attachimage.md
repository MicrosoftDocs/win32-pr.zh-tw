---
title: 'IVMDVDDrive AttachImage 方法 (VPCCOMInterfaces .h) '
description: 將 ISO 映像附加至 VM 內的 DVD 光碟機。
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- AttachImage 方法 Virtual PC
- AttachImage 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，AttachImage 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385150"
---
# <a name="ivmdvddriveattachimage-method"></a>IVMDVDDrive：： AttachImage 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將 ISO 映像連接至虛擬機器 (VM) 內的 DVD 光碟機。

## <a name="syntax"></a>語法


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*imagePath* \[在\]
</dt> <dd>

要附加之 ISO 映像的完整路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                    | Description                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                          | 作業成功。<br/>                                                                     |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>         | *ImagePath* 參數是目錄。<br/>                                                         |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>            | *ImagePath* 參數為 **Null**。<br/>                                                            |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>    | 找不到 VM。<br/>                                                                        |
| <dl> <dt>**VM \_\_ \_ \_ 使用中的 E 磁片磁碟機**</dt> <dt>0xA0040727</dt> </dl> | 主機 DVD 光碟機或 ISO 映像已附加至此磁片磁碟機。<br/>                                  |
| <dl> <dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt> </dl> | 此磁片磁碟機的匯流排位置無效，或磁片磁碟機似乎不是有效的 DVD 光碟機。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>    | 已發生未預期的錯誤。<br/>                                                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

