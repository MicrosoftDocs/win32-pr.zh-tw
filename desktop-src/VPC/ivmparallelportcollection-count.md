---
title: 'IVMParallelPortCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 此集合中的平行埠數目。
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMParallelPortCollection 介面
- IVMParallelPortCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934468"
---
# <a name="ivmparallelportcollectioncount-property"></a>IVMParallelPortCollection：： Count 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此集合中的平行埠數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>屬性值

平行埠的數目。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                            | 意義                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>               | 作業成功。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl> | 參數為 **Null**。<br/>    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection 定義為27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMParallelPortCollection**](ivmparallelportcollection.md)
</dt> </dl>

 

