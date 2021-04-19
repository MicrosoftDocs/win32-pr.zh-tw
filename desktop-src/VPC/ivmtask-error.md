---
title: 'IVMTask Error 屬性 (VPCCOMInterfaces) '
description: 抓取此工作所記錄的錯誤。
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Error 屬性 Virtual PC
- Error 屬性 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，Error 屬性
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965730"
---
# <a name="ivmtaskerror-property"></a>IVMTask：： Error 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此工作所記錄的錯誤。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a>屬性值

記錄的錯誤。

## <a name="error-codes"></a>錯誤碼

由其他介面傳回的 [**IVMTask**](ivmtask.md) 實例可能會傳回額外的值。 如需詳細資訊，請參閱傳回 **IVMTask** 實例之方法的檔。



| 名稱/值                                                                                                                                                                        | 意義                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                           | 作業成功。<br/>                              |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                             | 參數值為 **Null**。<br/>                           |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                     | 已發生未預期的錯誤。<br/>                          |
| <dl> <dt>VM \_E \_ VMVIRTUALPC \_ 較舊的 \_ 版本</dt> <dt>0xA0040952</dt> </dl>     | Virtual PC 2007 和 Windows Virtual PC 皆已安裝。<br/> |
| <dl> <dt>VM \_\_其他 \_ 虛擬化 \_ 軟體</dt> <dt>0xA0040953</dt> </dl> | 已安裝其他虛擬化軟體。<br/>                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

