---
title: 'IVMSerialPortCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 抓取此集合中的序列埠數目。
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMSerialPortCollection 介面
- IVMSerialPortCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8c7390b4637cf8e39fe83fcbb9844913a41d20fd2ed9515695ec068b33af6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593151"
---
# <a name="ivmserialportcollectioncount-property"></a>IVMSerialPortCollection：： Count 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此集合中的序列埠數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>屬性值

序列埠的數目。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                            | 意義                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>               | 作業成功。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl> | 參數為 **Null**。<br/>    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection 定義為 dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

