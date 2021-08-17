---
title: 'IVMVirtualPC CreateDifferencingVirtualHardDisk 方法 (VPCCOMInterfaces .h) '
description: 建立差異虛擬硬碟。
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- CreateDifferencingVirtualHardDisk 方法 Virtual PC
- CreateDifferencingVirtualHardDisk 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，CreateDifferencingVirtualHardDisk 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b065d7b1d7a5f5f21aa0120b58d4ca2dc9177d0a48f6b2389365ee37811883c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394418"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a>IVMVirtualPC：： CreateDifferencingVirtualHardDisk 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

建立差異虛擬硬碟。

## <a name="syntax"></a>語法


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*imagePath* \[在\]
</dt> <dd>

新磁片影像檔案的路徑。 如果未存在，將會建立包含的資料夾。

</dd> <dt>

*parentPath* \[在\]
</dt> <dd>

父磁片影像檔案的路徑。

</dd> <dt>

*diskTask* \[退出，retval\]
</dt> <dd>

用來追蹤影像建立的 [**IVMTask**](ivmtask.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | Description                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null**。<br/>                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt> </dl> | 系統找不到 *imagePath* 或 *parentPath* 參數所指定的路徑。<br/>                                                                                                                                             |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 不正確 \_ 磁片磁碟機)**</dt> <dt>0x8007000f</dt> </dl>   | *ImagePath* 參數所指定的檔案是在 CD-ROM 或 dvd-rom 上。<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>    | *ImagePath* 或 *parentPath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。<br/>                                                                                                                                |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>    | *ImagePath* 和 *parentPath* 參數都指定空的或相對路徑。 至少有一個參數必須是絕對路徑。<br/>                                                                                       |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl> | *ImagePath* 或 *parentPath* 參數所指定的路徑太長。 路徑長度必須少於260個字元。<br/>                                                                                              |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt> </dl>  | *ImagePath* 參數所參考的檔案已經存在。<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt> </dl>       | 動態擴充的虛擬硬碟映射在主機磁片區上需要至少 8 MB 的可用空間。<br/>                                                                                                                                      |
| <dl> <dt>**VM \_E \_ 影像 \_ 大小 \_ 太 \_ 大**</dt> <dt>0xA0040683</dt> </dl>                | 參數 *大小* 必須小於 2088960 MB。 如果格式為 FAT16，則大小必須小於 2000 MB。<br/>                                                                                                                   |
| <dl> <dt>**VM \_E \_ 影像 \_ 大小 \_ 太 \_ 小**</dt> <dt>0xA0040684</dt> </dl>                | 未格式化和 FAT16 格式化的虛擬硬碟映射必須至少為 3 MB。 FAT32 格式化的虛擬硬碟映射必須至少為 514 MB。<br/>                                                                                   |
| <dl> <dt>**VM \_E \_ 檔案 \_ 太 \_ 大 \_ ，無法進行 \_ 磁片**</dt>區 <dt>0xA0040679</dt> </dl>          | 如果動態擴充的虛擬硬碟映射擴展為其完整限制，則主機磁片區無法支援此大小的檔案。 FAT32 磁片區的檔案大小上限為 4 GB。 FAT16 磁片區的檔案大小上限為 2 GB。<br/> |
| <dl> <dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt> </dl>                    | 應用程式開始關機之後，無法建立虛擬硬碟。<br/>                                                                                                                                            |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl>     | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/>                                                                                                                                                |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a>備註

雖然 *imagePath* 或 *parentPath* 可以是相對路徑，但至少其中一個必須是絕對路徑。 如果一個路徑參數是相對路徑，則會假設為相對於另一個 path 參數。

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

 

