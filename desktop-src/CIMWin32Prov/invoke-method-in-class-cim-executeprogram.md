---
description: CIM ExecuteProgram 類別的 Invoke 方法 \_ 會採取特定的動作。 方法執行動作的詳細資料是特定的實作為。 此方法繼承自 CIM \_ 動作。
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: CIM_ExecuteProgram 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2945b3083060dfb4a3211771d53b770d3c4f574a0465003cf83a174a9d5c0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065098"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a>CIM ExecuteProgram 類別的 Invoke 方法 \_

[**CIM \_ ExecuteProgram**](cim-executeprogram.md)類別的 **Invoke** 方法會採取特定的動作。 方法執行動作的詳細資料是特定的實作為。 此方法繼承自 [**CIM \_ 動作**](cim-action.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Invoke();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。

## <a name="remarks"></a>備註

WMI 不會執行這個類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CIM \_ ExecuteProgram](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[**CIM \_ ExecuteProgram**](cim-executeprogram.md)
</dt> </dl>

 

