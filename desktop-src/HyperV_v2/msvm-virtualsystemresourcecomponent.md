---
description: 代表 Microsoft Windows hyper-v 平臺的虛擬裝置服務。
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0758858e9e45066cdfaddf36616c7861bbae914b12e3698665f8650c6c57d67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340168"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>Msvm \_ VirtualSystemResourceComponent 類別

代表 Microsoft Windows hyper-v 平臺的虛擬裝置服務。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemResourceComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemResourceComponent** 類別具有這些屬性。

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串陣列，其中包含這個 **Msvm \_ VirtualSystemResourceComponent** 實例所呈現的其他非關聯類別。 這些類別都必須衍生自 [**cim \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 或 [**cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

GUID，表示服務 COM 物件的類別識別碼。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。

</dd> <dt>

**內容**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

新建立的物件將在其中執行的內容。 此值會在 *dwClsCoNtext* 參數中傳遞至 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為1。

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果這個實例已啟用，而且可以用來完成用戶端要求，則為 **True** 。否則 **為 False**。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為 **True**。

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果這個實例可以熱新增至虛擬機器，則為 **True** ;否則 **為 False**。 預設值為 **False**。

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果可以從虛擬機器熱移除這個實例，則為 **True** ;否則 **為 False**。 預設值為 **False**。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

可唯一識別服務的語言中性字元串。 建議採用下列格式來防止命名衝突：「廠商 \| 元件 \| 版本」。 例如，此名稱代表 Microsoft 模擬網路埠元件的1.0 版：「Microsoft EmulatedNetworkPortComponent v1.0 \| 」 \| 。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用虛擬裝置在此處描述的 WMI 物件的關聯性。



| 值                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> 「<dt>**不可**</dt>變更」 <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> 「 <dt>**Singleton**</dt> 」 <dt>1</dt> </dl>                     | Singleton 是最上層的 WMI 物件，它會與虛擬裝置系結1:1，且每個虛擬機器只能存在一次。 這是預設值。<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"多重實例"**</dt> <dt>2</dt> </dl>     | 多重實例是最上層的 WMI 物件，每個虛擬機器可以多次存在，並與虛擬裝置系結1:1。<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdevice"**</dt> <dt>3</dt> </dl>                     | Subdevice 是沒有父參考的 WMI 物件，但只能由一個虛擬裝置所控制，每個虛擬機器只能存在一次。 但是 WMI 物件可以有倍數的時間。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualSystemResourceComponent** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 用戶端支援結束<br/>    | Windows 8.1<br/>                                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

