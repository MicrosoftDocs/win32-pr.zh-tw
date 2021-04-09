---
title: 'IVMHardDisk 父屬性 (VPCCOMInterfaces) '
description: 差異虛擬硬碟的父系。
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- 父屬性虛擬電腦
- 父屬性 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Parent 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933883"
---
# <a name="ivmharddiskparent-property"></a>IVMHardDisk：:P 不用屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取並設定差異虛擬硬碟的父系。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a>屬性值

設定與父硬碟影像相關聯的 [**IVMHardDisk**](ivmharddisk.md) 物件。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                               | 意義                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null**。<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                                               | 這不是差異硬碟，因此沒有父系。<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt> </dl> | 系統找不到父虛擬硬碟檔案。<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑) </dt> <dt>0x80070003</dt> </dl> | 系統找不到父虛擬硬碟檔案的路徑。<br/>                                                                                                                                                                                                   |
| <dl> <dt>VM \_E \_ HD \_ 映射 \_ 開啟 \_ 失敗</dt> <dt>0xA004067C</dt> </dl>                  | 嘗試開啟目前的硬碟影像檔案時發生錯誤。<br/>                                                                                                                                                                                               |
| <dl> <dt>VM \_電子 \_ HD \_ 影像 \_ 存取</dt> <dt>0xA0040681</dt> </dl>                      | 嘗試存取目前的硬碟影像檔案時發生錯誤。<br/>                                                                                                                                                                                             |
| <dl> <dt>VM \_E \_ 父系 \_ 子系 \_ 識別碼 \_ 不符</dt> <dt>0xA0040685</dt> </dl>            | *父* 參數所找出的虛擬硬碟映射與子磁片映射的識別碼不同。 請確定 *父* 參數所找到的父虛擬硬碟映射，與用來建立差異虛擬硬碟映射的映射相同。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>備註

這個屬性只適用于差異硬碟映射。

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

 

