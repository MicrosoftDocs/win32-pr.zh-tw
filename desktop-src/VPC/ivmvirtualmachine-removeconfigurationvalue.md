---
title: 'IVMVirtualMachine RemoveConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 移除此虛擬機器的指定設定設定值。
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- RemoveConfigurationValue 方法 Virtual PC
- RemoveConfigurationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RemoveConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466153"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a>IVMVirtualMachine：： RemoveConfigurationValue 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

移除此虛擬機器的指定設定設定值。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*configurationKey* \[在\]
</dt> <dd>

用來識別儲存在 ". .vmc" 檔案中之設定值的索引鍵 \* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                      | Description                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                            | 作業成功。<br/>       |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | 參數為 **Null** 或空白。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>      | 未知的設定。<br/>       |
| <dl> <dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt> </dl> | 找不到喜好設定。<br/>       |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>      | 已發生未預期的錯誤。<br/>   |



 

## <a name="remarks"></a>備註

這個方法會提供任何設定值的低層級存取權。 您可以使用它來移除客戶定義索引鍵的設定值。 如果您使用此方法移除系統設定值，請務必小心，因為當虛擬機器正在執行時，無法變更部分值。

設定金鑰位於虛擬機器的 " \* . .vmc" 檔案中（XML 格式）。 金鑰會以類似于 Windows 中登錄機碼的階層式方式儲存。 若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。

例如，若要移除 \_ 位於下列金鑰樹狀結構中「ram 大小」機碼的值：

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

*ConfigurationKey* 路徑字串的指定方式如下：

``` syntax
"hardware/memory/ram_size"
```

如果所需樹狀結構中的任何索引鍵具有 "id" 屬性值，則屬性和其值會在其相關聯的設定金鑰之後，緊接在 *configurationKey* 路徑字串中，並使用下列括弧格式： " \[ @id ="*id \_ value*" \] "。

例如，若要移除位於下列金鑰樹狀結構中的「絕對」索引鍵的值：

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

*ConfigurationKey* 路徑字串的指定方式如下：

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

