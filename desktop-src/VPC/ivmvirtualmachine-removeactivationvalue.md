---
title: 'IVMVirtualMachine RemoveActivationValue 方法 (VPCCOMInterfaces .h) '
description: 移除此虛擬機器之指定啟用設定的值。
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- RemoveActivationValue 方法 Virtual PC
- RemoveActivationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RemoveActivationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fcb531a405f66e39f9821e36f10d3e65e1e8b771472d87d0bce9e415dd672a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653028"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a>IVMVirtualMachine：： RemoveActivationValue 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

移除此虛擬機器之指定啟用設定的值。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*activationKey* \[在\]
</dt> <dd>

用來識別 .vmc 檔中所儲存之啟用值的索引鍵 \* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                      | 描述                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                            | 作業成功。<br/>                                                |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | 參數為 **Null** 或空白。<br/>                                          |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>      | 未知的設定。<br/>                                                |
| <dl> <dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt> </dl> | 找不到喜好設定，或此設定沒有有效的啟用。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>      | 已發生未預期的錯誤。<br/>                                            |



 

## <a name="remarks"></a>備註

此方法可提供任何啟用值的低層級存取權。 您可以使用它來移除客戶定義索引鍵的啟用值。 如果您使用此方法移除系統啟用值，請務必小心，因為當虛擬機器正在執行時，無法變更部分值。 當虛擬機器啟動時，會建立其設定值的複本，以成為其啟用值的集合。 啟用值會維持，直到虛擬機器關閉或重新開機為止。 請注意，Windows Virtual PC 可能只會使用設定來儲存特定金鑰的值，也就是可能永遠不會使用啟用值。

> [!Note]  
> 虛擬機器會話必須正在執行，才能變更任何啟用值。

 

啟用金鑰會以階層方式儲存在內部，類似于 Windows 中的登錄機碼。 若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。

例如，若要移除 \_ 位於下列金鑰樹狀結構中「預設動作」索引鍵的值：

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

*ActivationKey* 路徑字串的指定方式如下：

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

