---
title: 'IVMHardDisk Convert 方法 (VPCCOMInterfaces. h) '
description: 將固定大小的虛擬硬碟轉換成動態擴充的虛擬硬碟，或將動態擴充的虛擬硬碟轉換為固定大小的虛擬硬碟。
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- 轉換方法 Virtual PC
- Convert 方法 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Convert 方法
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e509c683ef86e169eb07d661c9682d8ed67204bcc7e1651d2d6370ee4be82f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593881"
---
# <a name="ivmharddiskconvert-method"></a>IVMHardDisk：： Convert 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將固定大小的虛擬硬碟轉換成動態擴充的虛擬硬碟，或將動態擴充的虛擬硬碟轉換為固定大小的虛擬硬碟。

## <a name="syntax"></a>語法


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*convertedDiskImagePath* \[在\]
</dt> <dd>

目標磁片影像檔案的路徑。

</dd> <dt>

*convertedDiskImageType* \[在\]
</dt> <dd>

目標磁片映射的類型。 如需值的清單，請參閱 [**VMHardDiskType**](vmharddisktype.md)。

</dd> <dt>

*convertTask* \[退出，retval\]
</dt> <dd>

[**IVMTask**](ivmtask.md)物件，用來追蹤轉換完成的轉換程式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                              | 描述                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                    | 作業成功。<br/>                                                                                                        |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | *ConvertedDiskImagePath* 參數是空的，或在檔案名上缺少 .vhd 副檔名。<br/>                                      |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                      | 參數為 **Null**。<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt> </dl>   | 系統找不到 *convertedDiskImagePath* 參數所指定的路徑。<br/>                                                 |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>      | *ConvertedDiskImagePath* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。<br/>                                    |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>      | *ConvertedDiskImagePath* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                            |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl>   | *ConvertedDiskImagePath* 參數所指定的路徑太長。 路徑必須小於 **最大 \_ 路徑** (260) 個字元。<br/> |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt> </dl> | 此物件參考的虛擬硬碟正在使用中，或此虛擬硬碟的父系正在使用中。<br/>                  |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt> </dl>         | 主機磁片區的空間不足，無法轉換此虛擬硬碟。<br/>                                                        |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt> </dl>    | *ConvertedDiskImagePath* 參數所參考的檔案已經存在。<br/>                                                        |
| <dl> <dt>**VM \_E \_ 錯誤的 \_ HD \_ 映射 \_ 類型**</dt> <dt>0xA004067B</dt> </dl>                   | *ConvertedDiskImagePath* 參數必須是 **VmDiskType \_ Dynamic** 或 **vmDiskType \_ FixedSize**。<br/>                          |
| <dl> <dt>**VM \_E \_ 不正確 \_ HD \_ FILE**</dt> <dt>0xA0040682</dt> </dl>                        | 這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射似乎不是有效的映射。<br/>          |
| <dl> <dt>**VM \_E \_ \_ \_ \_ 找不到父路徑**</dt> <dt>0xA0040677</dt> </dl>                 | 此物件參考的虛擬硬碟父系不存在。<br/>                                                        |
| <dl> <dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt> </dl>                      | 無法轉換虛擬硬碟映射，因為應用程式正在關閉。<br/>                                            |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                              | 已發生未預期的錯誤。<br/>                                                                                                    |



 

## <a name="remarks"></a>備註

在轉換程式之後，來源檔案會保持不變。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

