---
description: 代表 Microsoft Windows hyper-v 平臺的服務。
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Msvm_VirtualizationComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab2d2d5652f2969ad20ee70077d23375371e3507991a16b6d5e6dda2245678ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068428"
---
# <a name="msvm_virtualizationcomponent-class"></a>Msvm \_ VirtualizationComponent 類別

代表 Microsoft Windows hyper-v 平臺的服務。

下列語法已簡化受控物件格式 (MOF) 程式碼。

## <a name="syntax"></a>語法

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualizationComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualizationComponent** 類別具有這些屬性。

<dl> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**GUID** ，表示服務 COM 物件的類別識別碼。

</dd> <dt>

**內容**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：**實驗** 性
</dt> </dl>

新建立的物件將在其中執行的內容。 此值會在 *dwClsCoNtext* 參數中傳遞至 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。 此屬性一律設定為1。

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**True** 表示已啟用此實例，可用於完成用戶端要求;否則 **為 False**。 此屬性一律設定為 **True**。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

可唯一識別服務的語言中性字元串。 建議採用下列格式來防止命名衝突：「廠商 \| 元件 \| 版本」。 例如，此名稱代表 Microsoft 模擬網路埠元件的1.0 版：「Microsoft EmulatedNetworkPortComponent v1.0 \| 」 \| 。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualizationComponent** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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



 

