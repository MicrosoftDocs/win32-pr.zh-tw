---
title: 'IVMVirtualPC GetHardDisk 方法 (VPCCOMInterfaces .h) '
description: 抓取對應于現有磁片影像檔案的物件。
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- GetHardDisk 方法 Virtual PC
- GetHardDisk 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetHardDisk 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc57085662c62951032837db178888bac5cb4407b11d7777d2f165f7b9c5a100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136581"
---
# <a name="ivmvirtualpcgetharddisk-method"></a>IVMVirtualPC：： GetHardDisk 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取對應于現有磁片影像檔案的物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*imagePath* \[在\]
</dt> <dd>

現有磁片影像檔案的完整路徑。

</dd> <dt>

*硬碟* \[退出，retval\]
</dt> <dd>

對應至此磁片映射的 [**IVMHardDisk**](ivmharddisk.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                         |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | *ImagePath* 或 *硬碟* 參數為 **Null**。<br/>                                                                  |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt> </dl> | 系統找不到 *imagePath* 參數所指定的檔案。<br/>                                               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt> </dl> | 系統找不到 *imagePath* 參數所指定的路徑。<br/>                                               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>    | *ImagePath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。<br/>                                  |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>    | *ImagePath* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                          |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl> | *ImagePath* 參數所指定的路徑太長。 路徑長度必須少於260個字元。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                     |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl>     | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/>                                  |



 

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

 

