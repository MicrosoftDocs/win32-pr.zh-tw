---
description: 在 WMI 中註冊執行個體提供者。
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988316"
---
# <a name="__instanceproviderregistration-class"></a>\_\_InstanceProviderRegistration 類別

**\_ \_ InstanceProviderRegistration** 系統類別會在 WMI 中註冊執行個體提供者。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>成員

**\_ \_ InstanceProviderRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ InstanceProviderRegistration** 類別具有這些屬性。

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出類別或執行個體提供者會提供資料，或從 WMI 和通用訊息模型 (CIM) 存放庫中取出資料。 提取提供者支援動態存取其資料;和推送提供者會將其資料儲存在 CIM 存放庫中，並使用 WMI 來提供其存取權。 如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。 預設值是 0 (零)。

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**提取** (0) 


</dt> <dd>

提供者是提取提供者。

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**推送** (1) 


</dt> <dd>

提供者是推播提供者。

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2) 


</dt> <dd>

提供者是推播驗證的提供者。 請注意，目前不支援推播驗證提供者。

</dd> </dl>

</dd> <dt>

**供應商**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 提供者**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**\_ \_ 提供者**](--provider.md)實例的參考，表示執行個體提供者的物件路徑。 這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

提供者類型的陣列，包含查詢處理的支援。 類別提供者不支援所有類型的查詢。 如果執行個體提供者不支援查詢處理，則可以將 **QuerySupportLevels** 設定為 **Null** 。 支援查詢的提供者會執行 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法，並將此屬性設定為下列其中一個或多個值。

<dt>



  ( "WQL： UnarySelect" ) 


</dt> <dd></dd> <dt>



  ( "WQL： References" ) 


</dt> <dd></dd> <dt>



  ( "WQL： Associators of" ) 


</dt> <dd></dd> <dt>



  ( "WQL： V1ProviderDefined" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 True**，表示提供者支援資料刪除。

<dt>

對
</dt> <dd>

提供者藉由執行 [**iwbemservices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (類別提供者) 或 [**Iwbemservices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (執行個體提供者) ，支援類別或實例的刪除。

</dd> <dt>

否
</dt> <dd>

提供者不支援資料刪除，並傳回無法從 [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)或 [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 True**，表示提供者支援資料列舉。

<dt>



  (True) 


</dt> <dd>

提供者支援資料列舉，方法是實作為) 的 [**iwbemservices：： CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (類別提供者的其中一個，或) 的 [**Iwbemservices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (執行個體提供者。

</dd> <dt>



  (False) 


</dt> <dd>

提供者不支援資料列舉，並且會傳回無法從 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)或 [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 True**，則類別或執行個體提供者支援資料抓取。

<dt>

對
</dt> <dd>

提供者可透過執行 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來支援資料抓取。

</dd> <dt>

否
</dt> <dd>

提供者不支援資料抓取，並傳回無法從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 True**，則類別或執行個體提供者支援資料修改。

<dt>



  (True) 


</dt> <dd>

提供者藉由執行下列其中一種方法來支援類別或實例修改： [**iwbemservices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (類別提供者) 或 [**Iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (類別提供者) 。

</dd> <dt>



  (False) 


</dt> <dd>

提供者不支援資料修改，並傳回無法從 [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)或 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)進行的 **WBEM \_ E \_ 提供者 \_ \_** 。

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ InstanceProviderRegistration** 類別衍生自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)，它衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。 只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 **\_ \_ InstanceProviderRegistration** 的實例來註冊執行個體提供者。 只有系統管理員可以刪除提供者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_ObjectProviderRegistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[註冊類別提供者](registering-a-class-provider.md)
</dt> <dt>

[註冊執行個體提供者](registering-an-instance-provider.md)
</dt> </dl>

 

