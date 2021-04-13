---
title: 'IVMVirtualPC FindVirtualNetwork 方法 (VPCCOMInterfaces .h) '
description: 抓取符合所要求名稱的虛擬網路物件。
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- FindVirtualNetwork 方法 Virtual PC
- FindVirtualNetwork 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，FindVirtualNetwork 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509036"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>IVMVirtualPC：： FindVirtualNetwork 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取符合所要求名稱的虛擬網路物件。

## <a name="syntax"></a>語法


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*virtualNetworkName* \[在\]
</dt> <dd>

要尋找之虛擬網路的名稱。

</dd> <dt>

*virtualNetwork* \[退出，retval\]
</dt> <dd>

代表此虛擬網路之新 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | Description                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                        |
| <dl> <dt>**S \_FALSE**</dt> <dt>1</dt> </dl>                                               | 找不到指定的虛擬網路。<br/>                                    |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | *VirtualNetwork* 參數為 **Null** ，或找不到虛擬網路。<br/>   |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | *VirtualNetworkName* 參數無效或為空字串。<br/>               |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt> </dl> | 找不到虛擬網路檔案。<br/>                                         |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                    |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl>     | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |



 

## <a name="remarks"></a>備註

虛擬網路名稱不區分大小寫，例如 "MyNetwork" 和 "MyNetwork" 指的是相同的虛擬網路。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

