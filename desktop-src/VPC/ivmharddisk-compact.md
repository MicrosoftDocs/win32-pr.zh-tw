---
title: 'IVMHardDisk Compact 方法 (VPCCOMInterfaces .h) '
description: 壓縮動態擴充的虛擬硬碟映射。
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Compact 方法 Virtual PC
- Compact 方法 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Compact 方法
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686344"
---
# <a name="ivmharddiskcompact-method"></a>IVMHardDisk：： Compact 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

壓縮動態擴充的虛擬硬碟映射。

## <a name="syntax"></a>語法


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*compactTask* \[退出，retval\]
</dt> <dd>

用來追蹤完成壓縮進程的 [**IVMTask**](ivmtask.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                              | Description                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                    | 作業成功。<br/>                                                                                                        |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                              | 已發生未預期的錯誤。<br/>                                                                                                    |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                      | 參數為 **Null**。<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt> </dl> | 這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射正在使用中。<br/>                                  |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt> </dl>         | 主機磁片區的空間不足，無法建立壓縮此虛擬硬碟映射所需的暫存檔案。<br/>     |
| <dl> <dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt> </dl>                      | 無法壓縮虛擬硬碟映射，因為應用程式正在關閉。<br/>                                            |
| <dl> <dt>**VM \_E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                         | 這個 [**IVMHardDisk**](ivmharddisk.md) 物件所參考的虛擬硬碟映射會標示為唯讀。<br/>                     |
| <dl> <dt>**VM \_E \_ 錯誤的 \_ HD \_ 映射 \_ 類型**</dt> <dt>0xA004067B</dt> </dl>                   | 這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射必須是 **vmDiskTypeDynamic** 映射類型。<br/> |
| <dl> <dt>**VM \_E \_ 不正確 \_ HD \_ FILE**</dt> <dt>0xA0040682</dt> </dl>                        | 這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射似乎不是有效的映射。<br/>          |



 

## <a name="remarks"></a>備註

若要壓縮動態擴充的硬碟映射，應先將磁片映射上的可用空間清空。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

