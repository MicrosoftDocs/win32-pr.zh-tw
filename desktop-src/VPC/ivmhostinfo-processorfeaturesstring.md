---
title: 'IVMHostInfo ProcessorFeaturesString 屬性 (VPCCOMInterfaces .h) '
description: 抓取主機處理器所支援的清單功能。
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- ProcessorFeaturesString 屬性 Virtual PC
- ProcessorFeaturesString 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，ProcessorFeaturesString 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1040702df250c906bb32af5068a340c37a9ba3faabee3af17d8397bfdc8059e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998888"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>IVMHostInfo：:P rocessorFeaturesString 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取主機處理器所支援的清單功能。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>屬性值

以逗號分隔的功能清單。 例如，「MMX、SSE、SSE2、x86-64」。



| 值                                                                                 | 意義                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | 支援 AMD 虛擬化延伸模組。<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | 支援 Intel 虛擬化技術擴充功能。<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | 硬體輔助虛擬化已停用。<br/>            |
| <dl> <dt>使用</dt> </dl>     | 啟用硬體輔助虛擬化。<br/>             |
| <dl> <dt>™</dt> </dl>      | 支援 MMX 擴充功能。<br/>                             |
| <dl> <dt>SSE</dt> </dl>      | 支援 Streaming SIMD Extensions。<br/>                  |
| <dl> <dt>發揮</dt> </dl>     | 支援 Streaming SIMD Extensions 2。<br/>                |
| <dl> <dt>SSE3</dt> </dl>     | 支援 Streaming SIMD Extensions 3。<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | 支援受信任的執行技術擴充功能。<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | 支援 x86-64 擴充功能。<br/>                              |



 

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

