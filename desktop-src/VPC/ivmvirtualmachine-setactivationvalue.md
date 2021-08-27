---
title: 'IVMVirtualMachine SetActivationValue 方法 (VPCCOMInterfaces .h) '
description: 為此虛擬機器設定指定之啟用設定的值。
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- SetActivationValue 方法 Virtual PC
- SetActivationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，SetActivationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f7c669db848a668d294e509ad65a56ef19aebd53d0c718f12e524cfc16a940
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124718"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a>IVMVirtualMachine：： SetActivationValue 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

為此虛擬機器設定指定之啟用設定的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*activationKey* \[在\]
</dt> <dd>

用來識別 .vmc 檔中所儲存之啟用值的索引鍵 \* 。

</dd> <dt>

*activationValue* \[在\]
</dt> <dd>

啟用值。 這個值可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ UI4** (整數) 或 **vt \_ BOOL** (布林值) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                      | 描述                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                            | 作業成功。<br/>                                                                                       |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | *ActivationKey* 參數為 **Null** 或空白，或 *activationValue* 參數不是有效的 variant 類型。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>      | 未知的設定。<br/>                                                                                       |
| <dl> <dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt> </dl> | 設定沒有有效的啟用。<br/>                                                                          |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>      | 已發生未預期的錯誤。<br/>                                                                                   |



 

## <a name="remarks"></a>備註

此方法可提供任何啟用值的低層級存取權。 可以用來設定客戶定義之索引鍵的啟用值。 如果您使用這個方法來設定系統啟用值，就必須小心，因為啟動值不會執行錯誤檢查。 此外，當虛擬機器正在執行時，無法變更某些啟用值。 當虛擬機器啟動時，會建立其設定值的複本，以成為其啟用值的集合。 啟用值會維持，直到虛擬機器關閉或重新開機為止。 請注意，Windows Virtual PC 可能只會使用設定來儲存特定金鑰的值，也就是可能永遠不會使用啟用值。

> [!Note]  
> 虛擬機器會話必須正在執行，才能變更任何啟用值。

 

啟用金鑰會以階層方式儲存在內部，類似于 Windows 中的登錄機碼。 若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。

例如，若要設定 \_ 位於下列金鑰樹狀結構中「預設動作」索引鍵的值：

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

 

