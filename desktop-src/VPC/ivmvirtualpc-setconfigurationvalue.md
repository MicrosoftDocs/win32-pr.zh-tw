---
title: 'IVMVirtualPC SetConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 設定指定之設定的值。
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- SetConfigurationValue 方法 Virtual PC
- SetConfigurationValue 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，SetConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509035"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>IVMVirtualPC：： SetConfigurationValue 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

設定指定之設定的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*preferenceKey* \[在\]
</dt> <dd>

用來識別喜好設定的金鑰，會儲存在每個使用者的設定檔中， (Options.xml 于 "% LocalAppData% \\ Microsoft \\ WINDOWS Virtual PC" ) 。

> [!IMPORTANT]
> Options.xml 只能使用 **SetConfigurationValue** 方法進行變更。 不支援使用任何其他方法來變更 Options.xml。

 

</dd> <dt>

*preferenceValue* \[在\]
</dt> <dd>

喜好設定值。 這個值可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ UI4** (整數) 或 **vt \_ BOOL** (布林值) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                              | 作業成功。<br/>                                                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                | *PreferenceKey* 或 *PreferenceValue* 參數為 **Null**。<br/>                      |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | *PreferenceKey* 參數無效或為空字串。<br/>                    |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                        | 已發生未預期的錯誤。<br/>                                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                           | 目前的使用者沒有設定檔的足夠存取權。<br/>                  |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl> | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |



 

## <a name="remarks"></a>備註

*PreferenceKey* 參數支援下列值。



| *preferenceKey* 值      | Description                                                                                                                                                                           | 資料類型            | 預設值   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| 「閒置 \_ timeout」<br/> | 如果沒有作用中的 Vm 或應用程式正在使用 [Windows VIRTUAL PC 介面](virtual-pc-interfaces.md)，vpc.exe 應等候的秒數。<br/> | 等效<br/> | 30<br/> |



 

這個方法會提供任何設定值的低層級存取權。 可以用來設定客戶定義索引鍵的設定值。 如果您使用這個方法來設定系統組態值，請小心，因為設定值不會執行錯誤檢查。 此外，當虛擬機器正在執行時，某些設定值無法變更。

設定金鑰位於虛擬機器的「Options.xml」檔案中（XML 格式）。 金鑰會以類似于 Windows 中登錄機碼的階層式方式儲存。 若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。

例如，若要設定 \_ 位於下列金鑰樹狀結構中的「閒置 timeout」機碼值：

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

*PreferenceKey* 路徑字串的指定方式如下：

``` syntax
"idle_timeout"
```

如果所需樹狀結構中的任何索引鍵具有 "id" 屬性值，則屬性和其值會在其相關聯的設定金鑰之後，緊接在 *preferenceKey* 路徑字串中，並使用下列括弧格式： " \[ @id ="*id \_ value*" \] "。

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

*PreferenceKey* 路徑字串的指定方式如下：

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
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

