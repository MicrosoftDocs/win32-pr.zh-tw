---
title: 'IVMVirtualMachine SetConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 將此虛擬機器 (VM) 的指定設定值設定為。
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- SetConfigurationValue 方法 Virtual PC
- SetConfigurationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，SetConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965513"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>IVMVirtualMachine：： SetConfigurationValue 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將此虛擬機器 (VM) 的指定設定值設定為。

## <a name="syntax"></a>語法


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*configurationKey* \[在\]
</dt> <dd>

用來識別儲存在 ". .vmc" 檔案中之設定值的索引鍵 \* 。

> [!IMPORTANT]
> \*只有在使用 **SetConfigurationValue** 方法時，才應該對 ". .vmc" 進行變更。 \*不支援使用任何其他方法來變更 ". .vmc"。

 

</dd> <dt>

*configurationValue* \[在\]
</dt> <dd>

組態值。 這個值 cay 是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ UI4** (整數) 或 **vt \_ BOOL** (布林值) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | Description                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                                                                            |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | *ConfigurationKey* 參數為 **Null** 或空白，或 *configurationValue* 參數不是有效的 variant 類型。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl> | 未知的設定。<br/>                                                                                            |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                                                                        |



 

## <a name="remarks"></a>備註

*ConfigurationKey* 參數支援下列值。



| *configurationKey* 值                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 資料類型            | 預設值     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| 「 \_ \_ 開機時的硬體/bios/時間同步」 \_<br/>              | 如果 VM CMOS 時鐘要在開機時與主機時鐘同步處理，則為 "true";否則為 "false"。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | 布林<br/> | "true"<br/> |
| "integration/microsoft/host \_ time \_ sync/enabled" "<br/> | 如果在整合元件中啟用主機時間同步處理，則為 "true";否則為 "false"。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 布林<br/> | "true"<br/> |
| 「ui \_ 選項/自動 \_ 應用程式 \_ 發佈」<br/>                  | 如果整合元件中已啟用自動發行應用程式，則為 "true";否則為 "false"。 這也稱為虛擬應用程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 布林<br/> | "true"<br/> |
| 「 \_ \_ 要儲存的 ui 選項/秒」 \_<br/>                   | 關閉所有應用程式之後，儲存 VM 之前等候的秒數。 不過，低於20但超過4294968的值具有特殊意義。 如需詳細資訊，請參閱下列清單<br/> <dl> <dt><span id="0"></span>0</dt> <dd> 請勿儲存 VM。<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> 請等候20秒再儲存 VM。<br/> </dd> <dt><span id="214_294_967"></span>21 4294967</dt> <dd> 請等候指定的秒數，然後再儲存 VM。<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4294968 4294967295</dt> <dd> 請等候4294968秒，然後再儲存 VM。<br/> </dd> </dl> | 等效<br/> | 300<br/>    |



 

這個方法會提供任何設定值的低層級存取權。 可以用來設定客戶定義索引鍵的設定值。 如果您使用這個方法來設定系統組態值，請小心，因為設定值不會執行錯誤檢查。 此外，當虛擬機器正在執行時，某些設定值無法變更。

設定金鑰位於虛擬機器的 " \* . .vmc" 檔案中（XML 格式）。 金鑰會以類似于 Windows 中登錄機碼的階層式方式儲存。 若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。

例如，若要設定 \_ 位於下列金鑰樹狀結構中「ram 大小」機碼的值：

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

*ConfigurationKey* 路徑字串的指定方式如下：

``` syntax
"hardware/memory/ram_size"
```

如果所需樹狀結構中的任何索引鍵具有 "id" 屬性值，則屬性和其值會在其相關聯的設定金鑰之後，緊接在 *configurationKey* 路徑字串中，並使用下列括弧格式： " \[ @id ="*id \_ value*" \] "。

例如，若要設定位於下列金鑰樹狀結構中的 "高爾夫球" 索引鍵值：

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

*ConfigurationKey* 路徑字串的指定方式如下：

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
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
</dt> <dt>

[**IVMVirtualPC::SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

