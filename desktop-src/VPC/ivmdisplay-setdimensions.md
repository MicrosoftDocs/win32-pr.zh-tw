---
title: 'IVMDisplay SetDimensions 方法 (VPCCOMInterfaces .h) '
description: 設定 VM 顯示器的高度和寬度（以圖元為單位）。
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- SetDimensions 方法 Virtual PC
- SetDimensions 方法 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，SetDimensions 方法
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107000026"
---
# <a name="ivmdisplaysetdimensions-method"></a>IVMDisplay：： SetDimensions 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

設定虛擬機器 (VM) 顯示的高度和寬度（以圖元為單位）。

## <a name="syntax"></a>語法


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*displayPixelWidth* \[在\]
</dt> <dd>

寬度（以圖元為單位）。 值必須介於640到2048的值之間。 如果值未平均地除以8，則會縮減為下一個較低的8倍。

</dd> <dt>

*displayPixelHeight* \[在\]
</dt> <dd>

高度（以圖元為單位）。 值必須介於480到1920的值之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                    | Description                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | *DisplayPixelWidth* 參數無法平均地被8整除，或 *displayPixelWidth* 或 *displayPixelHeight* 參數超出允許的最小 (640) 或 2048x1920) 值上限。<br/> |
| <dl> <dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt> </dl>                     | 解決方式變更未及時完成。<br/>                                                                                                                                              |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>               | 虛擬機器必須正在執行，才能進行這種操作。<br/>                                                                                                                                               |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                    | 虛擬機器無效或目前未執行。<br/>                                                                                                                                         |
| <dl> <dt>**VM \_E \_ NO \_ DISPLAY**</dt> <dt>0xA0040850</dt> </dl>                    | 找不到 VM 的有效顯示。<br/>                                                                                                                                                          |
| <dl> <dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt> </dl> | 在客體作業系統中安裝的整合元件版本不支援這項操作。<br/>                                                                                    |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>備註

虛擬機器顯示的大小下限為 640 x 480 圖元。 大小上限為 2048 x 1920。 嘗試將顯示大小設定為超出這些限制的值，或設定為未平均整除8的任何寬度，會導致傳回 **電子 \_ INVALIDARG** 錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

