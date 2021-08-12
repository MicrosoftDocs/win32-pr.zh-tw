---
title: 'IVMFloppyDrive AttachImage 方法 (VPCCOMInterfaces .h) '
description: 將主機上的軟碟媒體映射連接到虛擬機器的磁片磁碟機。
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- AttachImage 方法 Virtual PC
- AttachImage 方法 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，AttachImage 方法
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21af305d0e7441fc931765795bb4e5d0785a211af6806ee80fd679d6f487b218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595712"
---
# <a name="ivmfloppydriveattachimage-method"></a>IVMFloppyDrive：： AttachImage 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將主機上的軟碟媒體映射連接到虛擬機器的磁片磁碟機。

## <a name="syntax"></a>語法


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mediaImagePath* \[在\]
</dt> <dd>

要附加之軟碟媒體映射的完整路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                                |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | *MediaImagePath* 參數無效。<br/>                                                                                 |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null**。<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | 沒有足夠的記憶體可完成此要求。<br/>                                                               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl> | *MediaImagePath* 參數所指定的路徑太長。 路徑必須小於 **最大 \_ 路徑** (260) 個字元。<br/> |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>    | *MediaImagePath* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。<br/>                                    |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>    | *MediaImagePath* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                            |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                            | 此虛擬機器的設定無效或找不到。<br/>                                                  |
| <dl> <dt>**VM \_E \_ 映射 \_ 捕捉 \_ 失敗**</dt> <dt>0xA00400650</dt> </dl>                  | 無法捕獲指定的影像檔案。<br/>                                                                              |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

