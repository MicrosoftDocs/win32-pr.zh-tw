---
title: 'IVMVirtualPC GetVirtualMachineFiles 方法 (VPCCOMInterfaces .h) '
description: 捕獲已知虛擬機器組態檔的陣列。
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- GetVirtualMachineFiles 方法 Virtual PC
- GetVirtualMachineFiles 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetVirtualMachineFiles 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ae2f96fb0c289f155158c77cdf3e4a8df1cb83aa8a51e0329d9fcd835ea4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998598"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a>IVMVirtualPC：： GetVirtualMachineFiles 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

捕獲已知虛擬機器組態檔的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*inAdditionalSearchPaths* \[在\]
</dt> <dd>

將會搜尋這些路徑，以及在 [**IVMVirtualPC：： SearchPaths**](ivmvirtualpc-searchpaths.md) 和 [**IVMVirtualPC：:D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) 屬性中設定的路徑。

</dd> <dt>

*inExcludedRegisteredVMs* \[在\]
</dt> <dd>

如果已註冊的虛擬機器應該從 *outVirtualMachineFileList* 參數的陣列傳回中排除，**則為 TRUE** ，否則為 **FALSE** 。

</dd> <dt>

*outVirtualMachineFileList* \[退出，retval\]
</dt> <dd>

在指定搜尋路徑中找到之虛擬機器組態檔案的路徑字串陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                        | 描述                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                              | 作業成功。<br/>                                                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                | *OutVirtualMachineFileList* 參數為 **Null**。<br/>                               |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | *InAdditionalSearchPaths* 參數不是字串的陣列。<br/>                  |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                        | 已發生未預期的錯誤。<br/>                                                    |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl> | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |



 

## <a name="remarks"></a>備註

用來抓取設定檔案陣列的搜尋路徑將包含 [**IVMVirtualPC：： SearchPaths**](ivmvirtualpc-searchpaths.md) 和 [**IVMVirtualPC：:D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) 之前的設定，除了 *inAdditionalSearchPaths* 參數所指定的路徑。

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

 

