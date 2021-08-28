---
title: 'IVMVirtualPC CreateFloppyDiskImage 方法 (VPCCOMInterfaces .h) '
description: 建立磁片影像檔案。
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- CreateFloppyDiskImage 方法 Virtual PC
- CreateFloppyDiskImage 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，CreateFloppyDiskImage 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1715bd9adc5fdcfae355b5992cb800a6d38a0889ed92745314daa6b2cfc2d8b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124657"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a>IVMVirtualPC：： CreateFloppyDiskImage 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

建立磁片影像檔案。

## <a name="syntax"></a>語法


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*imagePath* \[在\]
</dt> <dd>

新磁片影像檔案的完整路徑。 如果未存在，將會建立包含的資料夾。

</dd> <dt>

*imageType* \[在\]
</dt> <dd>

要建立的磁片映射類型。 只支援 **vmFloppyDiskImage \_ LowDensity** (1) 和 **vmFloppyDiskImage \_ HighDensity** (2) 。 請參閱 [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                                                                                         | 作業成功。<br/>                                                                                                                  |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | *ImagePath* 參數為 **Null**。<br/>                                                                                                         |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | *ImageType* 參數不是 [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) 或 **vmFloppyDiskImage \_ HighDensity** (2) 。<br/> |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt> </dl> | 系統找不到 *imagePath* 參數所指定的路徑。<br/>                                                                        |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>    | *ImagePath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。<br/>                                                           |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>    | *ImagePath* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                                                   |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl> | *ImagePath* 參數所指定的路徑太長。 路徑長度必須少於260個字元。<br/>                          |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt> </dl>  | 參數 *imagePath* 所參考的檔案已經存在。<br/>                                                                               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt> </dl>       | 主機磁片區上的空間不足，無法建立虛擬磁片映射。<br/>                                                        |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 發生意外錯誤。<br/>                                                                                                                  |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl>     | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/>                                                           |



 

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

 

