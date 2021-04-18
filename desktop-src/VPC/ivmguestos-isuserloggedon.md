---
title: 'IVMGuestOS IsUserLoggedOn 方法 (VPCCOMInterfaces .h) '
description: 判斷要求的會話是否存在。
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- IsUserLoggedOn 方法 Virtual PC
- IsUserLoggedOn 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，IsUserLoggedOn 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968740"
---
# <a name="ivmguestosisuserloggedon-method"></a>IVMGuestOS：： IsUserLoggedOn 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

判斷要求的會話是否存在。

## <a name="syntax"></a>語法


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*inRailSession* \[在\]
</dt> <dd>

針對鐵路會話設定為0，或針對 RDP 會話設定為1。

</dd> <dt>

*outSessionPresent* \[退出，retval\]
</dt> <dd>

如果會話存在，則設定為 **variant \_ TRUE** ，否則為 **variant \_ FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                       | Description                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                             | 作業成功。<br/>                                   |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                               | 參數為 **Null**。<br/>                                      |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                            | *OutSessionPresent* 參數無效或為 **Null**。<br/>  |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                       | 已發生未預期的錯誤。<br/>                               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl> | 沒有足夠的記憶體可完成此要求。<br/>  |
| <dl> <dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt> </dl>                        | 作業未及時完成。<br/>              |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                  | 虛擬機器 (VM) 必須針對此操作執行。<br/>    |
| <dl> <dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt> </dl>    | 此 VM 中未安裝整合元件功能。<br/> |
| <dl> <dt>**VM \_E \_ VM 已 \_ 暫停**</dt> <dt>0xA00400507</dt> </dl>                       | VM 已暫停。<br/>                                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

