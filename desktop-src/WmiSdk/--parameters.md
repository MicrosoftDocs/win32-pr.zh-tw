---
description: 定義方法的輸入和輸出參數。
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a2f39cb7b88977c8f61e562badaa6cbda7a5004fc2d0edf70eb59c6276070efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110563"
---
# <a name="__parameters-class"></a>\_\_PARAMETERS 類別

**\_ \_ 參數** 系統類別是定義方法之輸入和輸出參數的抽象類別。 它也可用來傳遞 WMI 用戶端與方法提供者之間的輸入和輸出參數值。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>成員

**\_ \_ PARAMETERS** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要定義使用者類別中的方法，WMI 用戶端會建立 **\_ \_ PARAMETERS** 類別的複本，並為方法中的每個輸入參數加入屬性。 如果方法包含傳回值或輸出參數，則必須建立 **\_ \_ 參數** 的另一個複本。 如果方法傳回傳回值，則用戶端必須加入名為 **ReturnValue** 的屬性。 然後，方法提供者會使用 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)的呼叫來儲存方法參數。

若要叫用方法，用戶端會依序呼叫下列各項：

1.  [**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) ，以抓取 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)儲存的 **\_ \_ PARAMETERS** 類別的複本。
2.  [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)，然後為方法的每個輸入參數設定一個屬性。
3.  [**Iwbemservices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) 或 [**Iwbemservices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) ，以執行方法。

在方法完成執行之後，如果方法有輸出參數或傳回值，則可能會傳回另一個 **\_ \_ 參數** 類別實例。

-   如果使用 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)叫用方法，則 **\_ \_ 參數** 實例會以 output 引數傳回。
-   如果使用 [**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)叫用方法，則 **\_ \_ 參數** 實例會以參數形式傳回給 [**IWbemObjectSink：：表示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 




